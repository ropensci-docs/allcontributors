# get_gh_issue_people

Extract lists of (1) all authors of, and (2) all contributors to, all
github issues for nominated repository, excluding issues closed as "not
planned"

## Usage

``` r
get_gh_issue_people(
  org,
  repo,
  exclude_issues = NULL,
  exclude_label = "wontfix",
  exclude_not_planned = TRUE
)
```

## Arguments

- org:

  Github organisation name for repository

- repo:

  Repository within `org` for which contributors are to be extracted

- exclude_issues:

  Numbers of any issues (or pull requests) to be excluded from lists of
  contributors.

- exclude_label:

  Exclude any contributions from issues with specified label (default =
  "wontfix"; set to `NULL` or empty string to include all issues).

- exclude_not_planned:

  If `TRUE` (default), exclude contributions to any issues closed as
  "not planned".

## Value

List of (authors, contributors), each as character vector of github
login names.

## See also

Other github:
[`get_gh_code_contributors()`](https://docs.ropensci.org/allcontributors/reference/get_gh_code_contributors.md),
[`get_gh_contrib_issue()`](https://docs.ropensci.org/allcontributors/reference/get_gh_contrib_issue.md),
[`get_gh_issue_titles()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_titles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
get_gh_issue_people (org = "ropensci", repo = "allcontributors")
} # }
```
