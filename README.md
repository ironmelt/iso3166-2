# ISO 3166-2 Database

This repository contains an up-to-date, complete collection of the data contained in the IS0 3166-2 Database, providing extensive information of all countries and their subdivisions around the world.

### Included data

The data contained includes information for all **assigned** country codes, with records provided in the following for:

```javascript
{
    "NO": {                         // ISO 3166-1 Alpha 2 country code
        "alpha2": "NO",             // ISO 3166-1 Alpha 2 country code (Repeated)
        "shortNameUppercase": "NORWAY",
                                    // Uppercase country name
        "shortName": "Norway",      // Short country name
        "officialName": "the Kingdom of Norway",
                                    // Official country name (nullable)
        "alpha3": "NOR",            // ISO 3166-1 Alpha 3 country code
        "un": "578",                // UN Country Code
                                    // See: https://unstats.un.org/unsd/methodology/m49/overview/
        "independent": true,        // True if the country is independent (UN source)
        "languages": [              // Localized country names
            {
                "alpha2": "nb",     // ISO 639-1 language code (nullable)
                                    // See: https://www.loc.gov/standards/iso639-2/php/English_list.php
                "alpha3": "nob",    // ISO 639-2 language code (nullable)
                                    // See: https://www.loc.gov/standards/iso639-2/php/English_list.php
                "localizedShortName": "Norge"
                                    // Localized country name
            },
            {
                "alpha2": "nn",
                "alpha3": "nno",
                "localizedShortName": "Noreg"
            }
        ],
        "subdivisions": [           // Country subdivisions
            {
                "type": "county",   // Subdivision type
                "iso": "NO-02",     // ISO 3166-2 subdivision code
                "name": "Akershus", // Subdivision name
                "language": "nn"    // ISO 639-1 language code (nullable)
            },
            {
                "type": "county",   // Note: subdivision can be present
                "iso": "NO-02",     // multiple times, when various translations
                "name": "Akershus", // are available for a given subdivision
                "language": "nb"
            },
            ...
            {
                "type": "arctic region",
                "iso": "NO-22",
                "name": "Jan Mayen (Arctic Region)",
                "language": "nb",
                "includedAs": "SJ"  // The region is also included in the ISO 3166-1
                                    // database with this code (nullable)
            },
        ],
    },
    "FR": {
        "subdivisions": [
            {
                "type": "metropolitan department",
                "iso": "FR-75",
                "name": "Paris",
                "language": "fr",
                "parent": "FR-IDF"  // Parent ISO 3166-2 subdivision code (nullable)
            },
            ...
        ],
        ...
    };
    "RS": {
        "subdivisions": [
            {
                "type": "city",
                "iso": "RS-00",
                "name": "Beograd",
                "language": "sr",
                "romanizationSystem": "UN III/11 1977"
                                    // The romanization system used to convert
                                    // the name to latin alphabet (nullable)
                                    // There may be multiple records for the same
                                    // region and the same language, but with
                                    // different romanization systems.
            },
            ...
        ],
        ...
    },
}
```

Overall, this database does follow the UN status for disputed territories and subdivisions.

### License

This database is made available under the Public Domain Dedication and License v1.0. Refer to the `LICENSE` file for more details.

### Source

All data is sourced from the [ISO Country Code Collection](https://www.iso.org/obp/ui/#iso:pub:PUB500001:en)