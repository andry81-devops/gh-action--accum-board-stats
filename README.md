<p align="center">
  <a href="https://github.com/andry81/gh-action--accum-board-stats/blob/master/userlog.md">Userlog</a>
• <a href="https://github.com/andry81/gh-action--accum-board-stats/blob/master/changelog.txt">Changelog</a>
• <a href="#dependecies">Dependencies</a>
• <a href="#known_issues">Known issues</a>
• <a href="#copyright-and-license"><img src="https://github.com/andry81/andry81/raw/master/badges/mit-license.svg" valign="middle" alt="copyright and license" />&nbsp;Copyright and License</a>
</p>

<h4 align="center">GitHub composite action to request and accumulate both the replies and the views statistic.<br/>
<br/>
Tutorial to use with: https://github.com/andry81/github-accum-stats</h4>

##

# gh-action--accum-board-stats@master

**Features**:

* Repository to track and repository to store traffic statistic can be different, and you may directly point the statistic as commits list:
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/board/phpbb`

* Workflow is used [accum-stats.sh](https://github.com/andry81/gh-workflow/blob/master/bash/board/accum-stats.sh) bash script to accumulate traffic statistic

* The script accumulates statistic both into a single file and into a set of files grouped by year and allocated per day:
  `traffic/board/phpbb/by_year/YYYY/YYYY-MM-DD.json`

# USAGE

> :warning: You must replace all placeholder into respective values:

* `{{REPO_OWNER}}` -> repository owner
* `{{REPO}}` -> your repository
* `{{TOPIC_KEYWORDS}}` -> topic keywords
* `{{TOPIC_AUTHOR}}` -> topic author

## Examples:

`./github/workflows/accum-phpbb-board-stats.yml`:

```yml
# based on: https://github.com/andry81/github-accum-stats
#

name: phpbb board stats updating every 4 hours

on:
  schedule:
    - cron: "0 */4 * * *"
  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

jobs:
  accum-phpbb-board-stats:
    runs-on: ubuntu-latest

    steps:
      - uses: {{REPO_OWNER}}/gh-action--accum-board-stats@master
        with:
          board_name:               phpbb
          # CAUTION: Beware of double quotes strip in case of usage yaml `>-` operator or even a single-quotted string!
          topic_query_url:          https://phpbb.com/board/search.php?keywords=\"{{TOPIC_KEYWORDS}}\"&terms=all&author={{TOPIC_AUTHOR}}&fid%5B%5D=6&sc=0&sf=titleonly&sr=topics&sk=i&sd=d&st=0&ch=1&t=0&submit=Search
          replies_sed_regexp:       s/.*class=\"posts\"[^0-9]*([0-9.]+).*/\1/p
          views_sed_regexp:         s/.*class=\"views\"[^0-9]*([0-9.]+).*/\1/p

          curl_flags: >-
            -H 'Cache-Control: no-cache'

          deps_repo_owner:          {{REPO_OWNER}}
          stat_entity_path:         traffic/board/phpbb

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}}--phpbb-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/board/phpbb
          output_repo_write_token:  ${{ secrets.READ_STATS_TOKEN }}
```

> :information_source: You can use `secrets.READ_STATS_TOKEN` instead of `secrets.WRITE_STATS_TOKEN` as long as both repositories under the same repository owner.

> :warning: You must use different values for `deps_repo_owner` and `output_repo_owner` if respective repositories actually under different repository owners.

> :information_source: See <a href="https://github.com/andry81/github-accum-stats/blob/master/README.md#reuse">REUSE</a> section for details if you have multiple repositories and want to store all workflow scripts in a single repository.

## Dependencies<a name="dependecies"></a>

* https://github.com/andry81/gh-workflow

## Known Issues<a name="known_issues"></a>

The action has supported not all features of a generic GitHub action: https://github.com/actions/runner/issues/646

> **What does Composite Run Steps Not Support**
>
> We don't support setting conditionals, continue-on-error, timeout-minutes, "uses", and secrets on individual steps within a composite action right now.
>
> (Note: we do support these attributes being set in workflows for a step that uses a composite run steps action)

## Copyright and License<a name="copyright-and-license"></a>

Code and documentation copyright 2021 Andrey Dibrov. Code released under [MIT License](https://github.com/andry81/gh-action--accum-gh-stats/blob/master/license.txt)
