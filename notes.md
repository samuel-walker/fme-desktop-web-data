# Using Web Data with FME Desktop

## Questions

1. FME Server involved at all? An extra step of installation etc. If we set up VMs it's no big deal though. Perhaps an optional step at the end to automate it? I think it probably shouldn't be involved at all. Maybe a quick bonus section for scheduling?

## Reminders

- Mention https://hashtagify.me
- Explain API quirks
-

## Learning Objectives

## Formats

- JSON
  - GeoJSON
    - Mapbox?
- XML
  - KML
- Hosted databases?
- Cesium Ion?
- WebMapTiler?
- WMS/WFS
- Image
  - MapnikRasterizer?
- Web connections/connectors
  - Tricky issue of accounts. Perhaps set it up with Google? Enough people have it?
  - Or just mention them, show example of how it would work

## Use-cases

- Social media data analysis
  - Customer locations
  - OGS Disaster Response Infrastructure?
    - Getting disaster-related data in central database?
    - Fitting to specification?
  - Sentiment analysis
    - NLP?
- Using fun APIs
  - [List here](https://docs.google.com/document/d/10tgBpnyGGBJ7qJfGKp3t11PszMrQnPG1O2db6XW3DZ4/edit#)
- US boundaries KMLs: https://www.census.gov/geo/maps-data/data/kml/kml_nation.html

## Skills

- Brief introduction to FME
  - Platform
  - Workspace components
  - Transformers
- Brief introduction to web data and web mapping?
  - Understanding GeoJSON format?
  - APIs?
- HTTPCaller
  - Basic GET, POST, PUT, and DELETE calls
  - Making actual API calls
    - Geocode, wiki info, Twitter, FME Server
- JSON transformers
  - JSONExtractor
  - JSONFlattener
  - JSONEFragmenter
  - JSONTemplater
  - JSONValidator
- XML transformers
  - Necessary to duplicate? Are these skills transferable? If not, which format is in higher demand?
  - Simply include same file as XML for testing purposes?

## Workflow

1. Read GeoJSON or JSON
  - From file on the web
2. Parse it into the right features using transformers
3. Make an API call to get other features
4. Join the GeoJSON and API features
5. Write out to HTML map using HTMLReportGenerator
  - Or to web map tiles
  - Or to WMS?

## Twitter example

- Forming direct link to Tweet for embedding
    - https://twitter.com/ + user.screen_name + /status/ + id

- Could try to allow CORS access, see http://www.enable-cors.org/server.html.

JSON Lint
JSON Query
Twitter API docs
Leaflet API docs
Maptime Boston

- Other attributes to consider:
  - _tweet_search_results.possibly_sensitive: false
	- _tweet_search_results.filter_level: "low"
