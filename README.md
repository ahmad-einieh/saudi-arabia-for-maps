# Saudi Arabia City Data

Text and Excel datasets for Saudi city coordinates and city-to-city distance/graph experiments. This repository contains data, not a runnable application or mapping API.

## Files

| File | Contents |
| --- | --- |
| [`allCities.txt`](allCities.txt) | 152 city-name rows |
| [`cities.txt`](cities.txt) | 371 weighted city-pair rows: `source destination distance` |
| [`cities2.txt`](cities2.txt) | 191 coordinate rows: `city longitude latitude` |
| [`cities with lon and lat.xlsx`](cities%20with%20lon%20and%20lat.xlsx) | Coordinate worksheets with city, longitude, and latitude columns |
| [`المدن.xlsx`](المدن.xlsx) | City/distance worksheets, including distance and air-distance columns |

Counts describe the checked-in text files, not guaranteed unique city totals. The files do not necessarily contain identical sets of cities.

## Text examples

```text
# cities.txt (the actual file has no header)
Riyadh Ad-Diriyah 39.72

# cities2.txt (the actual file has no header)
Mecca 39.826168 21.42251
```

Coordinate order is **longitude, latitude**. Many map libraries expect latitude first, so reorder values when necessary. City names in text commonly use hyphens; spelling/capitalization varies between datasets and worksheets.

## Use and limitations

Open spreadsheets in Excel/LibreOffice, or parse text rows with a whitespace-aware reader. Graph consumers must decide whether a listed connection is directed or bidirectional; that behavior is not encoded as a separate field.

Spreadsheet distance labels indicate kilometers in some cells, but units/formatting are not uniformly normalized. Sources, collection date, coordinate accuracy, and routing suitability are not fully documented. Validate and normalize data before analysis; do not treat this as an authoritative current road-distance or navigation dataset.
