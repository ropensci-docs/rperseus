# Get a primary text by URN.

Get a primary text by URN.

## Usage

``` r
get_perseus_text(urn, excerpt = NULL)
```

## Arguments

- urn:

  Valid uniform resource number (URN) obtained from
  [`perseus_catalog`](https://docs.ropensci.org/rperseus/reference/perseus_catalog.md).

- excerpt:

  An index to excerpt the text. For example, the first four "verses" of
  a text might be 1.1-1.4. If NULL, the entire work is returned.

## Value

A seven column `tbl_df` with one row for each "section" (splits vary
from text–could be line, chapter, etc.). Columns:

- text:

  character vector of text

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

  Text language, e.g. "grc" = Greek, "lat" = Latin, "eng" = English

- section:

  Text section or excerpt if specified

## Examples

``` r
get_perseus_text("urn:cts:greekLit:tlg0013.tlg028.perseus-grc2")
#> # A tibble: 18 × 7
#>    text                      urn   group_name label description language section
#>    <chr>                     <chr> <chr>      <chr> <chr>       <chr>      <int>
#>  1 Παλλάδ’ Ἀθηναίην, κυδρὴν… urn:… Homeric H… Hymn… Hymni Home… grc            1
#>  2 γλαυκῶπιν, πολύμητιν, ἀμ… urn:… Homeric H… Hymn… Hymni Home… grc            2
#>  3 παρθένον αἰδοίην, ἐρυσίπ… urn:… Homeric H… Hymn… Hymni Home… grc            3
#>  4 Τριτογενῆ, τὴν αὐτὸς ἐγε… urn:… Homeric H… Hymn… Hymni Home… grc            4
#>  5 σεμνῆς ἐκ κεφαλῆς, πολεμ… urn:… Homeric H… Hymn… Hymni Home… grc            5
#>  6 χρύσεα, παμφανόωντα· σέβ… urn:… Homeric H… Hymn… Hymni Home… grc            6
#>  7 ἀθανάτους· ἣ δὲ πρόσθεν … urn:… Homeric H… Hymn… Hymni Home… grc            7
#>  8 ἐσσυμένως ὤρουσεν ἀπ’ ἀθ… urn:… Homeric H… Hymn… Hymni Home… grc            8
#>  9 σείσασ’ ὀξὺν ἄκοντα· μέγ… urn:… Homeric H… Hymn… Hymni Home… grc            9
#> 10 δεινὸν ὑπὸ βρίμης γλαυκώ… urn:… Homeric H… Hymn… Hymni Home… grc           10
#> 11 σμερδαλέον ἰάχησεν· ἐκιν… urn:… Homeric H… Hymn… Hymni Home… grc           11
#> 12 κύμασι πορφυρέοισι κυκώμ… urn:… Homeric H… Hymn… Hymni Home… grc           12
#> 13 ἐξαπίνης· στῆσεν δ’ Ὑπερ… urn:… Homeric H… Hymn… Hymni Home… grc           13
#> 14 ἵππους ὠκύποδας δηρὸν χρ… urn:… Homeric H… Hymn… Hymni Home… grc           14
#> 15 εἵλετ’ ἀπ’ ἀθανάτων ὤμων… urn:… Homeric H… Hymn… Hymni Home… grc           15
#> 16 Παλλὰς Ἀθηναίη· γήθησε δ… urn:… Homeric H… Hymn… Hymni Home… grc           16
#> 17 καὶ σὺ μὲν οὕτω χαῖρε, Δ… urn:… Homeric H… Hymn… Hymni Home… grc           17
#> 18 αὐτὰρ ἐγὼ καὶ σεῖο καὶ ἄ… urn:… Homeric H… Hymn… Hymni Home… grc           18
get_perseus_text("urn:cts:latinLit:stoa0215b.stoa003.opp-lat1")
#> # A tibble: 69 × 7
#>    text                      urn   group_name label description language section
#>    <chr>                     <chr> <chr>      <chr> <chr>       <chr>      <int>
#>  1 f Tibique, Domine, celsu… urn:… Orientius… Orat… Orientius … lat            1
#>  2 et illa moles quadriform… urn:… Orientius… Orat… Orientius … lat            2
#>  3 te sempiterno confitentu… urn:… Orientius… Orat… Orientius … lat            3
#>  4 et nos imago consonantis… urn:… Orientius… Orat… Orientius … lat            4
#>  5 amen sonamus, alleluia d… urn:… Orientius… Orat… Orientius … lat            5
#>  6 Te septem primi deprecan… urn:… Orientius… Orat… Orientius … lat            6
#>  7 ceu ciuitatis septem pri… urn:… Orientius… Orat… Orientius … lat            7
#>  8 solio propinqui, ianitor… urn:… Orientius… Orat… Orientius … lat            8
#>  9 et nos imago consonantis… urn:… Orientius… Orat… Orientius … lat            9
#> 10 amen sonamus, alleluia d… urn:… Orientius… Orat… Orientius … lat           10
#> # ℹ 59 more rows
get_perseus_text(urn = "urn:cts:greekLit:tlg0031.tlg009.perseus-grc2", excerpt = "5.1-5.5")
#> # A tibble: 1 × 7
#>   text                       urn   group_name label description language section
#>   <chr>                      <chr> <chr>      <chr> <chr>       <chr>    <chr>  
#> 1 Τῇ ἐλευθερίᾳ ἡμᾶς Χριστὸς… urn:… New Testa… Gala… The New Te… grc      5.1-5.5
```
