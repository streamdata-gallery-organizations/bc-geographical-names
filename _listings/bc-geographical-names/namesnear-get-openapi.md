---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: BC Geographical Names Search near to a geographic point
  description: Search for information about geographical names that correspond to
    features within a geographic area defined by a centre point and a radius.  Various
    options and filter parameters are available to refine the search.
  contact:
    name: BC Geographical Names Office
    email: geographical.names@gov.bc.ca
  version: 3.x.x
host: apps.gov.bc.ca
basePath: /pub/bcgnws
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /featureCategories:
    get:
      summary: Get all feature categories
      description: 'Gets a list of all feature categories used by the BC Geographical
        Names Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-categories-used-by-the-bc-geographical-names-information-system-bcgnis---
      x-api-path-slug: featurecategories-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureCategories
  /featureClasses:
    get:
      summary: Get all feature classes
      description: 'Gets a list of all feature classes used by the BC Geographical
        Names Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-classes-used-by-the-bc-geographical-names-information-system-bcgnis---not
      x-api-path-slug: featureclasses-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureClasses
  /featureTypes:
    get:
      summary: Get all feature types
      description: 'Gets a list of all feature types used by the BC Geographical Names
        Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-types-used-by-the-bc-geographical-names-information-system-bcgnis---note-
      x-api-path-slug: featuretypes-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureTypes
  /features/{featureId}:
    get:
      summary: Get a feature by its featureId
      description: Get information about the geographical feature with the specified
        featureId.
      operationId: get-information-about-the-geographical-feature-with-the-specified-featureid-
      x-api-path-slug: featuresfeatureid-get
      parameters:
      - in: path
        name: featureId
        description: The unique identifier for a feature
      responses:
        200:
          description: OK
      tags:
      - Features
      - FeatureId
  /nameAuthorities:
    get:
      summary: Get all name authorities
      description: Gets a list of all name authorities responsible for naming decisions
        of the geographical names in the BC Geographical Names Information System
        (BCGNIS)
      operationId: gets-a-list-of-all-name-authorities-responsible-for-naming-decisions-of-the-geographical-names-in-th
      x-api-path-slug: nameauthorities-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - NameAuthorities
  /names/changes:
    get:
      summary: Search for names with metadata changes in a given period
      description: Search for information about geographical names which have changed
        most recently within a specified time window.  Changes may include status
        cupdates and metadata corrections.
      operationId: search-for-information-about-geographical-names-which-have-changed-most-recently-within-a-specified-
      x-api-path-slug: nameschanges-get
      parameters:
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: featureCategory
        description: A filter to limit the search to names associated with features
          of a certain category  The value of this parameter should be a featureCategoryCode
          value returned by the /featureCategories resource, or an asterisk (*) to
          request that all feature categories be included
      - in: query
        name: featureClass
        description: A filter to limit the search to names associated with features
          of a certain class  The value of this parameter should be a featureClassCode
          value returned by the /featureClasses resource, or an asterisk (*) to request
          that all feature classes be included
      - in: query
        name: featureType
        description: A filter to limit the search to names associated with features
          of a certain type  The value of this parameter should be a featureTypeCode
          value returned by the /featureTypes resource, or an asterisk (*) to request
          that all feature types be included
      - in: query
        name: fromDate
        description: Defines the earliest date (YYYY-MM-DD format) of the change time
          window for the search
      - in: query
        name: itemsPerPage
        description: The number of search results to return (1-200)
      - in: query
        name: outputFormat
        description: The format of the output
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: outputStyle
        description: A flag indicating whether to include with each matching name
          a succinct list of attributes (summary), or a comprehensive list of attributes
          (detail)
      - in: query
        name: sortBy
        description: The distance to move the accessPoint away from the curb and towards
          the inside of the parcel (in metres)
      - in: query
        name: startIndex
        description: The index of the first record to be returned (>= 1)
      - in: query
        name: toDate
        description: Defines the latest date (YYYY-MM-DD format) of the change time
          window for the search
      responses:
        200:
          description: OK
      tags:
      - Names
      - Changes
  /names/decisions/recent:
    get:
      summary: Search for names affected by recent naming decision
      description: Search for information about geographical names affected by naming
        'decisions' made by the BC Geographical Names Office (naming authority) within
        the last X days.
      operationId: search-for-information-about-geographical-names-affected-by-naming-decisions-made-by-the-bc-geograph
      x-api-path-slug: namesdecisionsrecent-get
      parameters:
      - in: query
        name: days
        description: The number of days used to define the time window of naming decisions
          to search
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: featureCategory
        description: A filter to limit the search to names associated with features
          of a certain category  The value of this parameter should be a featureCategoryCode
          value returned by the /featureCategories resource, or an asterisk (*) to
          request that all feature categories be included
      - in: query
        name: featureClass
        description: A filter to limit the search to names associated with features
          of a certain class  The value of this parameter should be a featureClassCode
          value returned by the /featureClasses resource, or an asterisk (*) to request
          that all feature classes be included
      - in: query
        name: featureType
        description: A filter to limit the search to names associated with features
          of a certain type  The value of this parameter should be a featureTypeCode
          value returned by the /featureTypes resource, or an asterisk (*) to request
          that all feature types be included
      - in: query
        name: itemsPerPage
        description: The number of search results to return (1-200)
      - in: query
        name: outputFormat
        description: The format of the output
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: outputStyle
        description: A flag indicating whether to include with each matching name
          a succinct list of attributes (summary), or a comprehensive list of attributes
          (detail)
      - in: query
        name: sortBy
        description: The distance to move the accessPoint away from the curb and towards
          the inside of the parcel (in metres)
      - in: query
        name: startIndex
        description: The index of the first record to be returned (>= 1)
      responses:
        200:
          description: OK
      tags:
      - Names
      - Decisions
      - Recent
  /names/decisions/year:
    get:
      summary: Search for names affected by naming decisions in a given year
      description: Search for information about geographical names affected by naming
        'decisions' made by the BC Geographical Names Office (naming authority) in
        a given year.
      operationId: search-for-information-about-geographical-names-affected-by-naming-decisions-made-by-the-bc-geograph
      x-api-path-slug: namesdecisionsyear-get
      parameters:
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: featureCategory
        description: A filter to limit the search to names associated with features
          of a certain category  The value of this parameter should be a featureCategoryCode
          value returned by the /featureCategories resource, or an asterisk (*) to
          request that all feature categories be included
      - in: query
        name: featureClass
        description: A filter to limit the search to names associated with features
          of a certain class  The value of this parameter should be a featureClassCode
          value returned by the /featureClasses resource, or an asterisk (*) to request
          that all feature classes be included
      - in: query
        name: featureType
        description: A filter to limit the search to names associated with features
          of a certain type  The value of this parameter should be a featureTypeCode
          value returned by the /featureTypes resource, or an asterisk (*) to request
          that all feature types be included
      - in: query
        name: itemsPerPage
        description: The number of search results to return (1-200)
      - in: query
        name: outputFormat
        description: The format of the output
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: outputStyle
        description: A flag indicating whether to include with each matching name
          a succinct list of attributes (summary), or a comprehensive list of attributes
          (detail)
      - in: query
        name: sortBy
        description: The distance to move the accessPoint away from the curb and towards
          the inside of the parcel (in metres)
      - in: query
        name: startIndex
        description: The index of the first record to be returned (>= 1)
      - in: query
        name: year
        description: The year in which to search for names affected by naming decisions
      responses:
        200:
          description: OK
      tags:
      - Names
      - Decisions
      - Year
  /names/inside:
    get:
      summary: Search in a geographic area
      description: Search for information about geographical names that correspond
        to features within a geographic bounding box.  Various options and filter
        parameters are available to refine the search.
      operationId: search-for-information-about-geographical-names-that-correspond-to-features-within-a-geographic-boun
      x-api-path-slug: namesinside-get
      parameters:
      - in: query
        name: bbox
        description: A geographic bounding box defining the search area
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: featureCategory
        description: A filter to limit the search to names associated with features
          of a certain category  The value of this parameter should be a featureCategoryCode
          value returned by the /featureCategories resource, or an asterisk (*) to
          request that all feature categories be included
      - in: query
        name: featureClass
        description: A filter to limit the search to names associated with features
          of a certain class  The value of this parameter should be a featureClassCode
          value returned by the /featureClasses resource, or an asterisk (*) to request
          that all feature classes be included
      - in: query
        name: featureType
        description: A filter to limit the search to names associated with features
          of a certain type  The value of this parameter should be a featureTypeCode
          value returned by the /featureTypes resource, or an asterisk (*) to request
          that all feature types be included
      - in: query
        name: itemsPerPage
        description: The number of search results to return (1-200)
      - in: query
        name: outputFormat
        description: The format of the output
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: outputStyle
        description: A flag indicating whether to include with each matching name
          a succinct list of attributes (summary), or a comprehensive list of attributes
          (detail)
      - in: query
        name: sortBy
        description: The distance to move the accessPoint away from the curb and towards
          the inside of the parcel (in metres)
      - in: query
        name: startIndex
        description: The index of the first record to be returned (>= 1)
      responses:
        200:
          description: OK
      tags:
      - Names
      - Inside
  /names/near:
    get:
      summary: Search near to a geographic point
      description: Search for information about geographical names that correspond
        to features within a geographic area defined by a centre point and a radius.  Various
        options and filter parameters are available to refine the search.
      operationId: search-for-information-about-geographical-names-that-correspond-to-features-within-a-geographic-area
      x-api-path-slug: namesnear-get
      parameters:
      - in: query
        name: distance
        description: A radius (in kilometres) around the centre point
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: featureCategory
        description: A filter to limit the search to names associated with features
          of a certain category  The value of this parameter should be a featureCategoryCode
          value returned by the /featureCategories resource, or an asterisk (*) to
          request that all feature categories be included
      - in: query
        name: featureClass
        description: A filter to limit the search to names associated with features
          of a certain class  The value of this parameter should be a featureClassCode
          value returned by the /featureClasses resource, or an asterisk (*) to request
          that all feature classes be included
      - in: query
        name: featurePoint
        description: A geographic coordinate specifying the centre point of the search
          area
      - in: query
        name: featureType
        description: A filter to limit the search to names associated with features
          of a certain type  The value of this parameter should be a featureTypeCode
          value returned by the /featureTypes resource, or an asterisk (*) to request
          that all feature types be included
      - in: query
        name: itemsPerPage
        description: The number of search results to return (1-200)
      - in: query
        name: outputFormat
        description: The format of the output
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: outputStyle
        description: A flag indicating whether to include with each matching name
          a succinct list of attributes (summary), or a comprehensive list of attributes
          (detail)
      - in: query
        name: sortBy
        description: The distance to move the accessPoint away from the curb and towards
          the inside of the parcel (in metres)
      - in: query
        name: startIndex
        description: The index of the first record to be returned (>= 1)
      responses:
        200:
          description: OK
      tags:
      - Names
      - Near
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---