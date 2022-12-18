<p align="center">
  <a href="#">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/shields-repo-size.svg" valign="middle" alt="GitHub repo size in bytes" /></a>
<!-- -- >
• <a href="#">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/shields-code-size.svg" valign="middle" alt="code size in bytes" /></a>
<!-- -->
• <a href="https://github.com/XAMPPRocky/tokei">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/tokei-lines-of-code.svg" valign="middle" alt="lines of code by tokei.rs" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-stats/gh-action--accum-board-stats--gh-stats/commits/master/traffic/views">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/views/all.svg" valign="middle" alt="GitHub views|any|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/views/all-14d.svg" valign="middle" alt="GitHub views|any|14d" /></a>
• <a href="https://github.com/andry81-stats/gh-action--accum-board-stats--gh-stats/commits/master/traffic/views">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/views/unq.svg" valign="middle" alt="GitHub views|unique per day|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/views/unq-14d.svg" valign="middle" alt="GitHub views|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-stats/gh-action--accum-board-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/clones/all.svg" valign="middle" alt="GitHub clones|any|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/clones/all-14d.svg" valign="middle" alt="GitHub clones|any|14d" /></a>
• <a href="https://github.com/andry81-stats/gh-action--accum-board-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/clones/unq.svg" valign="middle" alt="GitHub clones|unique per day|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/traffic/clones/unq-14d.svg" valign="middle" alt="GitHub clones|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-devops/gh-action--accum-board-stats/commits">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/commits-since-latest.svg" valign="middle" alt="GitHub commits since latest version" /></a>
  <a href="https://github.com/andry81-devops/gh-action--accum-board-stats/releases">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/latest-release-name.svg" valign="middle" alt="latest release name" /></a>
• <a href="https://github.com/andry81-devops/gh-action--accum-board-stats/releases">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-board-stats/badges/metrics/github-all-releases.svg" valign="middle" alt="GitHub all releases" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81/donate"><img src="https://github.com/andry81-cache/andry81--gh-content-cache/raw/master/common/badges/donate/donate.svg" valign="middle" alt="donate" /></a>
</p>

---

<p align="center">
  <a href="https://github.com/andry81-devops/gh-action--accum-board-stats/blob/master/userlog.md">Userlog</a>
• <a href="https://github.com/andry81-devops/gh-action--accum-board-stats/blob/master/changelog.txt">Changelog</a>
• <a href="#dependecies">Dependencies</a>
• <a href="#known-issues">Known issues</a>
• <a href="#copyright-and-license"><img src="https://github.com/andry81-cache/andry81--gh-content-cache/raw/master/common/badges/license/mit-license.svg" valign="middle" alt="copyright and license" />&nbsp;Copyright and License</a>
</p>

<h4 align="center">GitHub composite action to request and accumulate a forum board post replies and views statistic.<br/>
<br/>
Tutorial to use with: https://github.com/andry81-devops/accum-content</h4>

All tutorials: https://github.com/andry81/index#tutorials

##

# gh-action--accum-board-stats@master

**Features**:

* Repository to track and repository to store traffic statistic can be different, and you may directly point the statistic as commits list:
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/board/phpbb`

* Workflow is used [accum-stats.sh](https://github.com/andry81-devops/gh-workflow/blob/master/bash/board/accum-stats.sh) bash script to accumulate traffic statistic

* The script accumulates statistic both into a single file and into a set of files grouped by year and allocated per day:
  `traffic/board/phpbb/by_year/YYYY/YYYY-MM-DD.json`


**Functionality of the script**:

* Can treat invalid input or empty changes as not an error as by default (`CONTINUE_ON_INVALID_INPUT=1`, `CONTINUE_ON_EMPTY_CHANGES=1`)

* Can generate textual changelog file with notes about changes per commit (including changes absence in case of skipped errors; `ENABLE_GENERATE_CHANGELOG_FILE=1`)

* Can insert the time string in format `HH:MMZ` additionally after the date in each commit message (by default inserts only a date for shorter commit messages; `ENABLE_COMMIT_MESSAGE_DATE_WITH_TIME=1`)

* Can insert the workflow run number after date/time prefix in each commit message (by default does not insert for shorter commit messages; `ENABLE_COMMIT_MESSAGE_WITH_WORKFLOW_RUN_NUMBER=1`)

* Can print GitHub Actions Run URL (with workflow run number) into the changelog file to reference the log on the GitHub from the changelog file (`ENABLE_GITHUB_ACTIONS_RUN_URL_PRINT_TO_CHANGELOG=1`)

* Can print curl response in case of an error (by default only the progress prints; `ENABLE_PRINT_CURL_RESPONSE_ON_ERROR=1`)

# USAGE

> **Warning** You must replace all placeholder into respective values:

* `{{REPO_OWNER}}` -> repository owner
* `{{REPO}}` -> your repository
* `{{TOPIC_KEYWORDS}}` -> topic keywords
* `{{TOPIC_AUTHOR}}` -> topic author

## Examples:

<a name="accum-phpbb-board-stats-yml">`.github/workflows/accum-phpbb-board-stats.yml`</a>:

```yml
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
          # CAUTION: Beware of double quotes strip in case of usage yaml `>-` operator or even a single-quotted string!
          topic_query_url:          https://phpbb.com/board/search.php?keywords=\"{{TOPIC_KEYWORDS}}\"&terms=all&author={{TOPIC_AUTHOR}}&fid%5B%5D=6&sc=0&sf=titleonly&sr=topics&sk=i&sd=d&st=0&ch=1&t=0&submit=Search
          replies_sed_regexp:       s/.*class=\"posts\"[^0-9]*([0-9.]+).*/\1/p
          views_sed_regexp:         s/.*class=\"views\"[^0-9]*([0-9.]+).*/\1/p

          curl_flags: >-
            -v
            -H 'Cache-Control: no-cache'

          deps_repo_owner:          {{REPO_OWNER}}
          deps_repo_branch:         master
          deps_repo_read_token:     ${{ github.token }}

          commit_msg_entity:        my-board-1

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}}--phpbb-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/board/phpbb
          output_repo_write_token:  ${{ secrets.READ_STATS_TOKEN }}

          flags: >-
            ENABLE_PRINT_INITIAL_ENV_INTO_STDOUT=1

          env: >-
            ENABLE_GENERATE_CHANGELOG_FILE=1
            CHANGELOG_FILE=changelog.txt
            ENABLE_PRINT_CURL_RESPONSE_ON_ERROR=1
            ENABLE_COMMIT_MESSAGE_DATE_WITH_TIME=1            # insert the time string in format HH:MMZ additionally after the date in each commit message
            ENABLE_COMMIT_MESSAGE_WITH_WORKFLOW_RUN_NUMBER=1  # insert the workflow run number after date/time prefix in each commit message
            ENABLE_GITHUB_ACTIONS_RUN_URL_PRINT_TO_CHANGELOG=1
          #  ENABLE_YAML_DIFF_PRINT_AFTER_EDIT=1
          #  ENABLE_YAML_DIFF_PRINT_BEFORE_PATCH=1
          #  ERROR_ON_EMPTY_CHANGES_WITHOUT_ERRORS=1
          #  CONTINUE_ON_INVALID_INPUT=1
          #  CONTINUE_ON_EMPTY_CHANGES=1
```

> **Note** You can use `secrets.READ_STATS_TOKEN` instead of `secrets.WRITE_STATS_TOKEN` as long as both repositories under the same repository owner.

> **Warning** You must use different values for `deps_repo_owner` and `output_repo_owner` if respective repositories actually under different repository owners.

> **Note** See <a href="https://github.com/andry81-devops/github-accum-stats#reuse">REUSE</a> section for details if you have multiple repositories and want to store all GitHub workflow scripts (`.github/workflows/*.yml`) in a single repository.

## <a name="dependecies">Dependencies</a>

* https://github.com/andry81-devops/gh-workflow

## Known Issues

https://github.com/andry81-devops/accum-content#known-issues

## Last known issues updates

https://github.com/andry81-devops/accum-content#last-known-issues-updates

## <a name="copyright-and-license">Copyright and License</a>

Code and documentation copyright 2021 Andrey Dibrov. Code released under [MIT License](https://github.com/andry81-devops/gh-action--accum-board-stats/blob/master/license.txt)
