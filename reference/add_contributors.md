# add_contributors

Add contributors to README.Rmd

## Usage

``` r
add_contributors(
  repo = ".",
  ncols = 7,
  files = c("README.Rmd", "README.md"),
  type = c("code", "issues", "discussion"),
  exclude_label = "wontfix",
  exclude_issues = NULL,
  exclude_not_planned = TRUE,
  num_sections = 3,
  section_names = c("Code", "Issue Authors", "Issue Contributors"),
  format = "grid",
  check_urls = TRUE,
  alphabetical = FALSE,
  open_issue = FALSE,
  force_update = FALSE
)
```

## Arguments

- repo:

  Vector of repository locations for which contributions are to be
  extracted. Each location must be a git project with a github remote.
  Default is single repository in current working directory.

- ncols:

  Number of columns for contributors in 'README'

- files:

  Names of files in which to add contributors

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

- num_sections:

  Number of sections in which to divide contributors:

  - 1 All contributions within single section regardless of `type`

  - 2 Contributions divided between a single section for `code` and a
    second section for all other issue-related contributions.

  - 3 Contributions divided into single sections for each of the three
    `type` arguments.

- section_names:

  Names of the sections to appear on the nominated `files`.

- format:

  One of ("grid", "list", "text") to control display of contributors as

  - 1 "grid" for a rectangular grid, with each contributor represented
    by their github avatar, with avatar linked to contributor profile
    and name linked to repository contributions.

  - 2 "list" for a more condensed list with github user names only and
    no avatars, one contributor per line linked to issue contributions.

  - 3 "text" for a single line of text containing comma-separated github
    user names linked to issue contributions.

- check_urls:

  If `TRUE` (default), GitHub URLs of all contributors are checked to
  ensure they are still valid. (This is generally the most
  time-consuming stage, so set to 'FALSE' if you are sure all URLs are
  valid.)

- alphabetical:

  If `TRUE`, order contributors alphabetically, otherwise order by
  decreasing numbers of contributions.

- open_issue:

  If `TRUE`, open or edit an issue on github in order to notify all
  contributors that they've been added to your `README` (see Note).

- force_update:

  If `TRUE`, update the specified files even if contributions have not
  changed.

## Value

Named list of logical values indicating whether files of given names
were updated or not is returned invisibly (that is, only if explicitly
assigned to a return value).

## Note

Opening an issue on github requires the github command-line interface to
be locally installed. See <https://cli.github.com/>.

## See also

Other main:
[`get_contributors()`](https://docs.ropensci.org/allcontributors/reference/get_contributors.md)

## Examples

``` r
# The following code extracts the contributors from the git repository
# associated with current working directory and writes them to a file.
if (FALSE) { # \dontrun{
f <- tempfile (fileext = ".Rmd")
writeLines ("", f) # blank file in tempdir()
add_contributors (repo = ".", files = f)
} # }
```
