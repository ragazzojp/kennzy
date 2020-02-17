# Kennzy

Kennzy is a work in progress that will be described at a later stage.

Supported countries:

- `IT`: Italy

## Part 1: scraping license plates from Wikipedia

A set of Jupyter Notebooks are provided, one for each supported country,
that scrape Wikipedia for the list of license plates of a single country
and save the result in a file named `XX.json`, where `XX` stands for
the country identifier (see above).

The `.json` file has the following format:

```json
{
  "country": "XX",
  "categories": {
    "main": {
      "licensePlates": {
        "aa": {
          "name": "name of the place or organization corresponding to aa"
        },
        "bb": {
          "name": "name of the place or organization corresponding to bb"
        }
      }
    }
  }
}
```

License plates are grouped by category. The following categories
are currently supported:

- `main`: license plates of regular cars.
- `special`: government license plates and license plates of special organizations.
- `historical`: license plates of regular cars used no more.
