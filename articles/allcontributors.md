# allcontributors

The main functionality of the [`allcontributors`
package](https://github.com/ropensci/allcontributors) is described in
the main [`README`](https://docs.ropensci.org/allcontributors/). This
vignette provides a visual reference for the various options available
for formatting contributors.

## Default Grid Format

The following represents the default format of contributors divided into
three sections (“Code”, “Issue Authors”, and “Issue Contributors”), with
each section formatted as a grid with seven columns (determined by the
[`ncols`
parameter](https://docs.ropensci.org/allcontributors/reference/add_contributors.html)).
The images (“Avatars”) are hyperlinked to the main github pages of each
contributor, and the github names below them are linked to the
contributions made to the package by each contributor. The following
uses dummy avatars simply to reduce the compiled size of this vignette,
and also uses dummy names for all except the first. (The names are dummy
only in the sense of being entirely generic, although they actually do
belong to real people - click to find out.)

### Code

[TABLE]

### Issue Authors

[TABLE]

### Issue Contributors

[TABLE]

------------------------------------------------------------------------

## Section Organisation

The default output shown above has three sections of “Code”, “Issue
Authors” and “Issue Contributors”. The organisation of these sections
can be controlled by the parameters `num_sections`, `type`, and
`section_names`.

The `type` parameter enables sections to be removed by reducing them
from the default three referred to as `code`, `issues` (for those who
open issues), and `discussion` (for those who contribute to issues). For
example, passing `type = "code"` will only acknowledge direct
contributions to code, while ignoring all those who contributed to
issues only.

The `num_sections` argument is provided for convenience, primarily in
order to allow default formats to have either one, two, or three
sections. Specifying `num_sections = 2` will by default collapse the
“Issue Authors” and “Issue Contributors” sections into a single section
named “Issues”. (This section title may be renamed with the
`section_names` parameter.)

## List Format

The `format` parameter of the [`add_contributors()`
function](https://docs.ropensci.org/allcontributors/reference/add_contributors.html)
accepts the three options of “grid”, “list”, or “text.” With the three
default section titles as shown above, the “list” option gives output
that looks like this:

### Code

1.  [mpadge](https://github.com/ropensci/allcontributors/commits?author=mpadge)
2.  [this-person](https://github.com/ropensci/allcontributors/commits?author=this-person)
3.  [that-person](https://github.com/ropensci/allcontributors/commits?author=that-person)
4.  [somebody](https://github.com/ropensci/allcontributors/commits?author=somebody)
5.  [somebody-else](https://github.com/ropensci/allcontributors/commits?author=somebody-else)
6.  [them](https://github.com/ropensci/allcontributors/commits?author=them)
7.  [others](https://github.com/ropensci/allcontributors/commits?author=others)

### Issue Authors

1.  [nobody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anobody)
2.  [somebody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Asomebody)
3.  [anybody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Aanybody)
4.  [nope](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anope)
5.  [yep](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Ayep)
6.  [maybe](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Amaybe)
7.  [doubtful](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Adoubtful)

### Issue Contributors

1.  [here](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Ahere)
2.  [there](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Athere)
3.  [anywhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Aanywhere)
4.  [somewhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asomewhere)
5.  [nowhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Anowhere)
6.  [sometime](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asometime)
7.  [later](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Alater)

## Text Format

Finally, the text format enables contributors to be acknowledged as a
single lines of text.

### Code

[mpadge](https://github.com/ropensci/allcontributors/commits?author=mpadge),
[this-person](https://github.com/ropensci/allcontributors/commits?author=this-person),
[that-person](https://github.com/ropensci/allcontributors/commits?author=that-person),
[somebody](https://github.com/ropensci/allcontributors/commits?author=somebody),
[somebody-else](https://github.com/ropensci/allcontributors/commits?author=somebody-else),
[them](https://github.com/ropensci/allcontributors/commits?author=them),
[others](https://github.com/ropensci/allcontributors/commits?author=others)

### Issue Authors

[nobody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anobody),
[somebody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Asomebody),
[anybody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Aanybody),
[nope](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anope),
[yep](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Ayep),
[maybe](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Amaybe),
[doubtful](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Adoubtful)

### Issue Contributors

[here](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Ahere),
[there](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Athere),
[anywhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Aanywhere),
[somewhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asomewhere),
[nowhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Anowhere),
[sometime](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asometime),
[later](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Alater)

The shortest possible way of acknowledging your contributors would be
like this:

``` r

add_contributors (num_sections = 1, format = "text")
```

which would in this case convert the above into the single list of,

[mpadge](https://github.com/ropensci/allcontributors/commits?author=mpadge),
[this-person](https://github.com/ropensci/allcontributors/commits?author=this-person),
[that-person](https://github.com/ropensci/allcontributors/commits?author=that-person),
[somebody](https://github.com/ropensci/allcontributors/commits?author=somebody),
[somebody-else](https://github.com/ropensci/allcontributors/commits?author=somebody-else),
[them](https://github.com/ropensci/allcontributors/commits?author=them),
[others](https://github.com/ropensci/allcontributors/commits?author=others),
[nobody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anobody),
[somebody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Asomebody),
[anybody](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Aanybody),
[nope](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Anope),
[yep](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Ayep),
[maybe](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Amaybe),
[doubtful](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+author%3Adoubtful),
[here](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Ahere),
[there](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Athere),
[anywhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Aanywhere),
[somewhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asomewhere),
[nowhere](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Anowhere),
[sometime](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Asometime),
[later](https://github.com/ropensci/allcontributors/issues?q=is%3Aissue+commenter%3Alater)
