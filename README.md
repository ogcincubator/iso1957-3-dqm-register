# ISO19157-3 Data Quality Measures Register

This repository contains:

* automation tooling to ingest a draft register from content included as a submodule
* a original demo pipeline configuration to semantically uplift a Google Spreadsheet containing ISO19157-3 properties.

The content is (currently) pushed to a staging/development node of the OGC Rainbow as a set of related vocabularies linked together by identifiers.

[http://defs-dev.opengis.net/vocprez-hosted/vocab/?filter=iso19157]()

e.g. http://defs-dev.opengis.net/vocprez-hosted/object?uri=https%3A//standards.isotc211.org/19157/-3/1/req/content/qualityMeasure

# ISO 19157-3 register ingest

A set of sheets are ingested from CSV sources into a set of graphs that combine to form a complete register complete with multivalued complex properties for examples, formulae etc.


# Demo from spreadsheet
## Files

### content files

### configuration
- `.ogc/`: OGC tools configuration
  - `config.yml`: General configuration (download URLs and target files) 
  - `catalog.ttl`: Domain Configuration catalog with uplift definition for `*.csv.json` files.
- `csv2python.yml`: Uplift definition that simply turns CSV into JSON
- `properties-uplift.yml`: Uplift definition that takes the JSONified CSV and converts it to JSON-LD and Turtle
- `.github/workflows/`: GitHub workflows
  - `uplift-and-join.yaml`: Converts CSV to Linked Data with cross references between elemennts
  - `pus-to-rainbow.yaml`: 

## See also

- [OGC Naming Authority tools (ogc-na)](https://opengeospatial.github.io/ogc-na-tools/)
  - [Domain configuration and uplift context examples](https://opengeospatial.github.io/ogc-na-tools/examples/)
  - [ingest_json reference](https://opengeospatial.github.io/ogc-na-tools/reference/ogc/na/ingest_json/)
  - [CSV input filter configuration](https://opengeospatial.github.io/ogc-na-tools/reference/ogc/na/input_filters/csv/)
