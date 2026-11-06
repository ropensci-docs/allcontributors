# get_gh_code_contributors

Get list of all code contributors to the code of a repository

## Usage

``` r
get_gh_code_contributors(org, repo, alphabetical = FALSE)
```

## Arguments

- org:

  Github organisation name for repository

- repo:

  Repository within `org` for which contributors are to be extracted

- alphabetical:

  If `TRUE`, order contributors alphabetically, otherwise order by
  decreasing numbers of contributions.

## Value

A `data.frame` of two columns of contributor (name, login)

## See also

Other github:
[`get_gh_contrib_issue()`](https://docs.ropensci.org/allcontributors/reference/get_gh_contrib_issue.md),
[`get_gh_issue_people()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_people.md),
[`get_gh_issue_titles()`](https://docs.ropensci.org/allcontributors/reference/get_gh_issue_titles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
get_gh_code_contributors (org = "ropensci", repo = "allcontributors")
} # }
```
