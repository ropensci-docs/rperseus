# Render a text parallel with ggplot2

Render a text parallel with ggplot2

## Usage

``` r
perseus_parallel(perseus_df, words_per_row = 6)
```

## Arguments

- perseus_df:

  a data frame obtained from `get_perseus_text`. Can contain multiple
  texts.

- words_per_row:

  adjusts the words displayed per "row".

## Value

a ggplot object

## Examples

``` r
if (FALSE) { # \dontrun{
tibble::tibble(label = c("Colossians", rep("1 Thessalonians", 2), "Romans"),
               excerpt = c("1.4", "1.3", "5.8", "8.35-8.39")) %>%
 dplyr::left_join(perseus_catalog) %>%
 dplyr::filter(language == "grc") %>%
 dplyr::select(urn, excerpt) %>%
 as.list() %>%
 purrr::pmap_df(get_perseus_text) %>%
 perseus_parallel()
} # }
```
