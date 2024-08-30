# Notes

## Version 1.0.0

### Third submission

> Please omit the \donttest. The if(interactive()) wrap is enough to
indicate that it's only supposed to run interactively.

> So, in this case, is it really supposed to run interactively? If not
please omit if(interactive()).
>
> Otherwise, donttest{} is unnecessary since calls wrapped in
if(interactive()) are not run by example() or automated checks anyway.

The example includes a way to generate an input dataset using an external
package (`clusterProfiler`), which takes longer than 5 seconds to execute.
We decided to remove the `if(interactive())` condition from the example.

### Second submission

> If there are references describing the methods in your package, please
add these in the description field of your DESCRIPTION file in the form
authors (year) <doi:...>
authors (year) <arXiv:...>
authors (year, ISBN:...)
or if those are not available: <https:...>
with no space after 'doi:', 'arXiv:', 'https:' and angle brackets for
auto-linking. (If you want to add a title as well please put it in
quotes: "Title")

Added the reference in the description field.

> \dontrun{} should only be used if the example really cannot be executed
(e.g. because of missing additional software, missing API keys, ...) by
the user. That's why wrapping examples in \dontrun{} adds the comment
("# Not run:") as a warning for the user. Does not seem necessary.
Please replace \dontrun with \donttest.
> 
> Please unwrap the examples if they are executable in < 5 sec, or replace
dontrun{} with \donttest{}.

Wrapped examples with `\donttest{}` instead of `\dontrun{}`. 

### R CMD check results

0 errors | 0 warnings | 1 note

* This is a new release.
