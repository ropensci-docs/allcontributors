# get_contributors

Get all contributors to a repository, including those who contribute to
code, open issues, and contribute to discussions in issues.

## Usage

``` r
get_contributors(
  org,
  repo,
  type = c("code", "issues", "discussion"),
  exclude_label = "wontfix",
  exclude_issues = NULL,
  exclude_not_planned = TRUE,
  alphabetical = FALSE,
  rm_ctbs_ptn = "(\\-(bot|actions)$|dependabot)",
  check_urls = TRUE,
  quiet = FALSE
)
```

## Arguments

- org:

  Github organisation name for repository

- repo:

  Repository within `org` for which contributors are to be extracted

- type:

  Type of contributions to include: 'code' for direct code contributions
  (including documentation), 'issues' to recognise contributors who open
  issues, and 'discussion' for contributing to discussions within
  issues. Discussion contributions are only from individuals not present
  in either 'issues' or 'code'; and 'issues' contributions are only from
  individuals not present in 'code'.

- exclude_label:

  Exclude any contributions from issues with specified label (default =
  "wontfix"; set to `NULL` or empty string to include all issues).

- exclude_issues:

  Numbers of any issues (or pull requests) to be excluded from lists of
  contributors.

- exclude_not_planned:

  If `TRUE` (default), exclude contributions to any issues closed as
  "not planned".

- alphabetical:

  If `TRUE`, order contributors alphabetically, otherwise order by
  decreasing numbers of contributions.

- rm_ctbs_ptn:

  Remove contributors which match this pattern (such as "actions-bot",
  or "ropensci-review-bot").

- check_urls:

  If `TRUE` (default), GitHub URLs of all contributors are checked to
  ensure they are still valid. (This is generally the most
  time-consuming stage, so set to 'FALSE' if you are sure all URLs are
  valid.)

- quiet:

  If `FALSE`, display progress information on screen.

## See also

Other main:
[`add_contributors()`](https://docs.ropensci.org/allcontributors/reference/add_contributors.md)

## Examples

``` r
if (FALSE) { # \dontrun{
get_contributors (org = "ropensci", repo = "allcontributors")
} # }
```
