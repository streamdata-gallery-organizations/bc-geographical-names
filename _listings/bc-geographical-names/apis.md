---
name: BC Geographical Names
x-slug: bc-geographical-names
description: Geographical names are more than labels on maps and road signs. They
  can reveal patterns of settlement, exploration and migration, and mirror outside
  influences to our history - aspects of the heritage and promise of an area that
  might otherwise be overlooked or forgotten by visitors and later generations.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
x-kinRank: "7"
x-alexaRank: "0"
tags: BC Geographical Names
created: "2018-08-29"
modified: "2018-08-29"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/apis.md
specificationVersion: "0.14"
apis:
- name: BC Geographical Names - Get all feature categories
  x-api-slug: featurecategories-get
  description: 'Gets a list of all feature categories used by the BC Geographical
    Names Information System (BCGNIS).  Note: there are three levels of classification
    in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset
    of a category, and a category is a subset of a class.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featurecategories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featurecategories-get-openapi.md
- name: BC Geographical Names - Get all feature classes
  x-api-slug: featureclasses-get
  description: 'Gets a list of all feature classes used by the BC Geographical Names
    Information System (BCGNIS).  Note: there are three levels of classification in
    the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset
    of a category, and a category is a subset of a class.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featureclasses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featureclasses-get-openapi.md
- name: BC Geographical Names - Get all feature types
  x-api-slug: featuretypes-get
  description: 'Gets a list of all feature types used by the BC Geographical Names
    Information System (BCGNIS).  Note: there are three levels of classification in
    the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset
    of a category, and a category is a subset of a class.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featuretypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featuretypes-get-openapi.md
- name: BC Geographical Names - Get a feature by its featureId
  x-api-slug: featuresfeatureid-get
  description: Get information about the geographical feature with the specified featureId.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featuresfeatureid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/featuresfeatureid-get-openapi.md
- name: BC Geographical Names - Get all name authorities
  x-api-slug: nameauthorities-get
  description: Gets a list of all name authorities responsible for naming decisions
    of the geographical names in the BC Geographical Names Information System (BCGNIS)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/nameauthorities-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/nameauthorities-get-openapi.md
- name: BC Geographical Names - Search for names with metadata changes in a given
    period
  x-api-slug: nameschanges-get
  description: Search for information about geographical names which have changed
    most recently within a specified time window.  Changes may include status cupdates
    and metadata corrections.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/nameschanges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/nameschanges-get-openapi.md
- name: BC Geographical Names - Search for names affected by recent naming decision
  x-api-slug: namesdecisionsrecent-get
  description: Search for information about geographical names affected by naming
    'decisions' made by the BC Geographical Names Office (naming authority) within
    the last X days.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesdecisionsrecent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesdecisionsrecent-get-openapi.md
- name: BC Geographical Names - Search for names affected by naming decisions in a
    given year
  x-api-slug: namesdecisionsyear-get
  description: Search for information about geographical names affected by naming
    'decisions' made by the BC Geographical Names Office (naming authority) in a given
    year.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesdecisionsyear-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesdecisionsyear-get-openapi.md
- name: BC Geographical Names - Search in a geographic area
  x-api-slug: namesinside-get
  description: Search for information about geographical names that correspond to
    features within a geographic bounding box.  Various options and filter parameters
    are available to refine the search.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesinside-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesinside-get-openapi.md
- name: BC Geographical Names - Search near to a geographic point
  x-api-slug: namesnear-get
  description: Search for information about geographical names that correspond to
    features within a geographic area defined by a centre point and a radius.  Various
    options and filter parameters are available to refine the search.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnear-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnear-get-openapi.md
- name: BC Geographical Names - Search by name, limit to unofficial names only
  x-api-slug: namesnotofficialsearch-get
  description: Search for information about unofficial geographical names by the text
    of the name itself.  Various options and filter parameters are available to refine
    the search.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnotofficialsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnotofficialsearch-get-openapi.md
- name: BC Geographical Names - Search by name, limit to official names only
  x-api-slug: namesofficialsearch-get
  description: Search for information about official geographical names by the text
    of the name itself.  Various options and filter parameters are available to refine
    the search.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesofficialsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesofficialsearch-get-openapi.md
- name: BC Geographical Names - Search by name
  x-api-slug: namessearch-get
  description: Search for information about geographical names by the text of the
    name itself.  The response will include both official and unofficial names.  Various
    options and filter parameters are available to refine the search.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namessearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namessearch-get-openapi.md
- name: BC Geographical Names - Get a name by its nameId
  x-api-slug: namesnameid-outputformat-get
  description: Get information about the geographical name with the specified nameId.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnameid-outputformat-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/namesnameid-outputformat-get-openapi.md
- name: Geo Mark Web Service - Create a new geomark by copying the geometries from
    one or more existing geomarks from the current server.
  x-api-slug: geomarkscopy-post
  description: The source geomarks can be specified by with the geomarkUrl parameter.  Repeat
    the parameter if sourcing from multiple geomarks
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarkscopy-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarkscopy-post-openapi.md
- name: Geo Mark Web Service - Create a new geomark
  x-api-slug: geomarksnew-post
  description: Create a new geomark from the geometries read from the 'body' parameter
    or file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksnew-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksnew-post-openapi.md
- name: Geo Mark Web Service - Get information about a particular geomark
  x-api-slug: geomarksgeomarkid-fileformatextension-get
  description: The attribution can be downloaded as a info file format. The download
    files can then be processed by a client application to access the geomark info
    fields and to get the URLs to the geometry download resources.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkid-fileformatextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkid-fileformatextension-get-openapi.md
- name: Geo Mark Web Service - Gets the bounding box of the geomark
  x-api-slug: geomarksgeomarkidboundingbox-fileformatextension-get
  description: The source geomarks can be specified by with the geomarkUrl parameter.  Repeat
    the parameter if sourcing from multiple geomarks
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidboundingbox-fileformatextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidboundingbox-fileformatextension-get-openapi.md
- name: Geo Mark Web Service - Get the feature and attribution of the geomark
  x-api-slug: geomarksgeomarkidfeature-fileformatextension-get
  description: The geomark feature resource returns a single spatial feature with
    either a single (Point, LineString, Polygon) or multi-part geometry (MultiPoint,
    MultiLineString, MultiPolygon) and the geomark attribution.  The geometry and
    attribution can be downloaded as a spatial download file format in a supported
    coordinate system. The download files can then be used in a desktop GIS application
    (e.g. ArcMap), Google Earth or a web mapping application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidfeature-fileformatextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidfeature-fileformatextension-get-openapi.md
- name: Geo Mark Web Service - Get the individual geometries within a multi-part geometry
  x-api-slug: geomarksgeomarkidparts-fileformatextension-get
  description: The geomark parts resource returns a one or more spatial features.
    One for each part of the Geomark's geomerty. Each part contains a single (Point,
    LineString, Polygon) geometry and the geomark attribution.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidparts-fileformatextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidparts-fileformatextension-get-openapi.md
- name: Geo Mark Web Service - Gets a single spatial point representative of the geomark.
  x-api-slug: geomarksgeomarkidpoint-fileformatextension-get
  description: The geomark point resource returns a single spatial feature with a
    single Point and the geomark attribution.  The point geometry will be created
    from the first geometry part of the Geomark. Point geomarks will return the first
    Point part in the geomark.  LineString geomarks will return the first coordinate
    of the first LineString part in the geomark. Polygon geomarks will return the
    centroid or another point inside the first Polygon part in the geomark. The geometry
    and attribution can be downloaded as a spatial download file format in a supported
    coordinate system. The download files can then be used in a desktop GIS application
    (e.g. ArcMap), Google Earth or a web mapping application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/british-columbia.png
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/geomark
  tags: Geo, Geography, Locations, API Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidpoint-fileformatextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/bc-geographical-names/master/_listings/bc-geographical-names/geomarksgeomarkidpoint-fileformatextension-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://bbc.api.gallery.streamdata.io
- type: x-api-stack
  url: http://bc.geographical.names.stack.network
- type: x-website
  url: https://apps.gov.bc.ca/pub/bcgnws/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---