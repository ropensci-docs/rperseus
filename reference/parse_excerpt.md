# Parse a Greek excerpt

This function parses a Greek excerpt from the Perseus Digital Library.
Parsing includes part of speech, gender, case, mood, voice, tense,
person, number, and degree.

## Usage

``` r
parse_excerpt(urn, excerpt)
```

## Arguments

- urn:

  a valid urn from the perseus_catalog object.

- excerpt:

  a valid excerpt, e.g. 5.1-5.5

## Value

a data frame

## Examples

``` r
parse_excerpt("urn:cts:greekLit:tlg0031.tlg002.perseus-grc2", "5.1-5.4")
#> # A tibble: 73 × 12
#>    word  form  verse part_of_speech person number tense mood  voice gender case 
#>    <chr> <chr> <chr> <chr>          <chr>  <chr>  <chr> <chr> <chr> <chr>  <chr>
#>  1 καί   Καὶ   5.1   conjunction    NA     NA     NA    NA    NA    NA     NA   
#>  2 ἔρχο… ἦλθον 5.1   verb           third  plural aori… indi… acti… NA     NA   
#>  3 εἰς   εἰς   5.1   preposition    NA     NA     NA    NA    NA    NA     NA   
#>  4 ὁ     τὸ    5.1   article        NA     singu… NA    NA    NA    neuter accu…
#>  5 πέραν πέραν 5.1   adverb         NA     NA     NA    NA    NA    NA     NA   
#>  6 ὁ     τῆς   5.1   article        NA     singu… NA    NA    NA    femin… gena…
#>  7 θάλα… θαλά… 5.1   noun           NA     singu… NA    NA    NA    femin… gena…
#>  8 εἰς   εἰς   5.1   preposition    NA     NA     NA    NA    NA    NA     NA   
#>  9 ὁ     τὴν   5.1   article        NA     singu… NA    NA    NA    femin… accu…
#> 10 χώρα  χώραν 5.1   noun           NA     singu… NA    NA    NA    femin… accu…
#> # ℹ 63 more rows
#> # ℹ 1 more variable: degree <chr>
```
