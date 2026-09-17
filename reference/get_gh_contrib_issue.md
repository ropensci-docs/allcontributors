# get_gh_contrib_issue

Extract contributors currently listed on an "All Contributions" issue in
a github repository.

## Usage

``` r
get_gh_contrib_issue(org, repo)
```

## Arguments

- org:

  Github organisation name for repository

- repo:

  Repository within `org` for which contributors are to be extracted

## Value

Character vector of github logins for all contributors listed in current
issue, or empty character string if there no issue named "All
Contributors".

## See also

Other github:
[`get_gh_code_contributors()`](https://docs.ropensci.org/allcontributors/reference/get_gh_code_contributors.md),
[`get_gh_issue_people()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_people.md),
[`get_gh_issue_titles()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_titles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
get_gh_contrib_issue (org = "ropensci", repo = "allcontributors")
} # }
```
