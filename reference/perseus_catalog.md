# Metadata for texts available via the Perseus Digital Library.

A dataset containing the texts available from the Perseus Digital
Library.

## Usage

``` r
perseus_catalog
```

## Format

A data frame with 2291 rows and 5 variables:

- urn:

  Uniform Resource Number

- group_name:

  Could refer to author (e.g. "Aristotle") or corpus (e.g. "New
  Testament")

- label:

  Text label, e.g. "Phaedrus"

- description:

  Text description

- language:

  Text language, e.g. "grc" = Greek, "lat" = Latin, "eng" = English,
  "hpt" = Hebrew pointed text, "hct" = Hebrew consonantal text, "ger" =
  German, "oth" = other

## Source

<http://cts.perseids.org/api/cts/?request=GetCapabilities>
