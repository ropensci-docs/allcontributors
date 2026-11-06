# get_gh_issue_titles

Extract titles and numbers of all issues associated with a nominated
repository

## Usage

``` r
get_gh_issue_titles(org, repo)
```

## Arguments

- org:

  Github organisation name for repository

- repo:

  Repository within `org` for which contributors are to be extracted

## Value

`data.frame` with one column of issue numbers, and one column of issue
titles.

## See also

Other github:
[`get_gh_code_contributors()`](https://docs.ropensci.org/allcontributors/reference/get_gh_code_contributors.md),
[`get_gh_contrib_issue()`](https://docs.ropensci.org/allcontributors/reference/get_gh_contrib_issue.md),
[`get_gh_issue_people()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_people.md)

## Examples

``` r
if (FALSE) { # \dontrun{
get_gh_issue_titles (org = "ropensci", repo = "allcontributors")
} # }
```
