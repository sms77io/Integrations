# @datafire/refugerestrooms
REFUGE is a web application that seeks to provide safe restroom access for transgender, intersex, and gender nonconforming individuals.

## Operation: v1.restrooms.json.get
Get all restroom records ordered by date descending.

### Input Schema
```json
{
  "type": [
    "object",
    "null"
  ],
  "properties": {
    "page": {
      "type": "integer",
      "description": "Page offset to fetch."
    },
    "per_page": {
      "type": "integer",
      "description": "Number of results to return per page."
    },
    "offset": {
      "type": "integer",
      "description": "Pad a number of results."
    },
    "ada": {
      "type": "boolean",
      "description": "Only return restrooms that are ADA accessible."
    },
    "unisex": {
      "type": "boolean",
      "description": "Only return restrooms that are unisex."
    }
  },
  "additionalProperties": false
}
```
### Output Schema
```json
{}
```
## Operation: v1.restrooms.by_date.json.get
Search for restroom records updated or created on or after a given date

### Input Schema
```json
{
  "type": "object",
  "properties": {
    "page": {
      "type": "integer",
      "description": "Page offset to fetch."
    },
    "per_page": {
      "type": "integer",
      "description": "Number of results to return per page."
    },
    "offset": {
      "type": "integer",
      "description": "Pad a number of results."
    },
    "ada": {
      "type": "boolean",
      "description": "Only return restrooms that are ADA accessible."
    },
    "unisex": {
      "type": "boolean",
      "description": "Only return restrooms that are unisex."
    },
    "updated": {
      "type": "boolean",
      "description": "Return restroom records updated (rather than created) since given date"
    },
    "day": {
      "type": "integer",
      "description": "Day"
    },
    "month": {
      "type": "integer",
      "description": "Month"
    },
    "year": {
      "type": "integer",
      "description": "Year"
    }
  },
  "additionalProperties": false,
  "required": [
    "day",
    "month",
    "year"
  ]
}
```
### Output Schema
```json
{}
```
## Operation: v1.restrooms.by_location.json.get
Search by location.

### Input Schema
```json
{
  "type": "object",
  "properties": {
    "page": {
      "type": "integer",
      "description": "Page offset to fetch."
    },
    "per_page": {
      "type": "integer",
      "description": "Number of results to return per page."
    },
    "offset": {
      "type": "integer",
      "description": "Pad a number of results."
    },
    "ada": {
      "type": "boolean",
      "description": "Only return restrooms that are ADA accessible."
    },
    "unisex": {
      "type": "boolean",
      "description": "Only return restrooms that are unisex."
    },
    "lat": {
      "type": "number",
      "format": "float",
      "description": "latitude"
    },
    "lng": {
      "type": "number",
      "format": "float",
      "description": "longitude"
    }
  },
  "additionalProperties": false,
  "required": [
    "lat",
    "lng"
  ]
}
```
### Output Schema
```json
{}
```
## Operation: v1.restrooms.search.json.get
Perform full-text search of restroom records.

### Input Schema
```json
{
  "type": "object",
  "properties": {
    "page": {
      "type": "integer",
      "description": "Page offset to fetch."
    },
    "per_page": {
      "type": "integer",
      "description": "Number of results to return per page."
    },
    "offset": {
      "type": "integer",
      "description": "Pad a number of results."
    },
    "ada": {
      "type": "boolean",
      "description": "Only return restrooms that are ADA accessible."
    },
    "unisex": {
      "type": "boolean",
      "description": "Only return restrooms that are unisex."
    },
    "query": {
      "type": "string",
      "description": "Your search query."
    }
  },
  "additionalProperties": false,
  "required": [
    "query"
  ]
}
```
### Output Schema
```json
{}
```