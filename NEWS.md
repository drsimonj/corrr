# corrr 0.2.1.9000

## Small breaking changes

The `diagonal` argument of `as_matrix` and `as_matrix.cor_df` is now an optional argument rather than set to `1` by default [#52](https://github.com/drsimonj/corrr/issues/52)

## New Functions

- `as_cordf` will coerce lists or matrices into correlation data frames if possible.
- `focus_if` enables conditional variable selection.

## New Functionality

- Can use arithmetic operators (e.g., `+` or `-`) with correlation data frames.
- Plotting functions (`rplot` and `network_plot`) will attempt to coerce objects to a correlation data frame (via `as_cordf`) if needed, making it possible to directly use these functions with other square-matrix-like objects.
- `repel` option added to `network_plot` (default = `TRUE`).
- `curved` option added to `network_plot` (default = `TRUE`).
- `correlate()` now prints a message about the `method` and `use` parameters. Can be silenced with `quiet = TRUE`.
- `correlate()` now supports data frame with a SQL back-end (`tbl_sql`)

## Fixes

- When `legend = TRUE` (now the default setting), `rplot` and `network_plot` generate a single, unlabelled legend referring to the size of the correlations.

## Other

- `correlate()` is now an S3 method so that it can adapt to `x`'s object type.

- During the development of this version, ggplot v2.2.0 was released. Many changes in the plotting functions have been made to handle new features in the updated version of ggplot2.

# corrr 0.2.1

## New Functionality

- Can keep leading zeros when using `fashion()` with new argument `leading_zeros = TRUE`.
- New optional arguments added to plotting functions, `network_plot()` and `rplot()`:
  - `legend` to display a legend mapping correlations to size and colour.
  - `colours` (or `colors`) to change colours in plot.

## Fixes

- `network_plot()` no longer plots wrong colours if only positive correlations are included.
- Colour scheme for `network_plot()` changed to match `rplot()`.
- Other bug fixes.

# corrr 0.2.0

## New Functions

- `network_plot()` the correlations.
- `focus_()` for standard evaluation version of `focus()`.

## New Functionality

- `fashion()` will now attempt to work on any object (not just `cor_df`), making it useful for printing any data frame, matrix, vector, etc.
- `print_cor` argument added to `rplot()` to overlay the correlations as text.

## Other

- `na_omit` argument in `stretch()` changed to `na.rm` to match `gather_()`.
- Bug fixes.
- Improvements.

# corrr 0.1.0

- First corrr release!
