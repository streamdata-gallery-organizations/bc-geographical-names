swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 1
info:
  title: Geo Mark Web Service
  description: the-geomark-web-service-allows-you-to-create-and-share-geographic-areas-of-interest-over-the-web-in-a-variety-of-formats-and-coordinate-systems--this-service-is-especially-helpful-when-you-need-to-share-an-area-of-interest-with-people-who-require-that-the-data-be-in-a-different-format-or-they-use-different-mapping-software-
  termsOfService: http://www2.gov.bc.ca/gov/content/governments/about-the-bc-government/databc/open-data/api-terms-of-use-for-ogl-information
  contact:
    name: Data BC
    url: http://data.gov.bc.ca/
    email: DataBCBA@gov.bc.ca
  version: 4.1.2
host: apps.gov.bc.ca
basePath: /pub/geomark
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
  /names/notOfficial/search:
    get:
      summary: Search by name, limit to unofficial names only
      description: Search for information about unofficial geographical names by the
        text of the name itself.  Various options and filter parameters are available
        to refine the search.
      operationId: search-for-information-about-unofficial-geographical-names-by-the-text-of-the-name-itself---various-
      x-api-path-slug: namesnotofficialsearch-get
      parameters:
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: exactSpelling
        description: If the name parameter is specified, exactSpelling specifies whether
          to include only names that exactly match the search text (exactSpelling=1),
          or whether to also include names with similar spellings (exactSpelling=0)
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
        name: name
        description: A filter to search based on the the text of the name itself
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
      - NotOfficial
      - Search
  /names/official/search:
    get:
      summary: Search by name, limit to official names only
      description: Search for information about official geographical names by the
        text of the name itself.  Various options and filter parameters are available
        to refine the search.
      operationId: search-for-information-about-official-geographical-names-by-the-text-of-the-name-itself---various-op
      x-api-path-slug: namesofficialsearch-get
      parameters:
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: exactSpelling
        description: If the name parameter is specified, exactSpelling specifies whether
          to include only names that exactly match the search text (exactSpelling=1),
          or whether to also include names with similar spellings (exactSpelling=0)
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
        name: name
        description: A filter to search based on the the text of the name itself
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
      - Official
      - Search
  /names/search:
    get:
      summary: Search by name
      description: Search for information about geographical names by the text of
        the name itself.  The response will include both official and unofficial names.  Various
        options and filter parameters are available to refine the search.
      operationId: search-for-information-about-geographical-names-by-the-text-of-the-name-itself---the-response-will-i
      x-api-path-slug: namessearch-get
      parameters:
      - in: query
        name: embed
        description: A flag to indicate whether to embed the corresponding feature
          into each matching name
      - in: query
        name: exactSpelling
        description: If the name parameter is specified, exactSpelling specifies whether
          to include only names that exactly match the search text (exactSpelling=1),
          or whether to also include names with similar spellings (exactSpelling=0)
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
        name: name
        description: A filter to search based on the the text of the name itself
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
      - Search
  /names/{nameId}.{outputFormat}:
    get:
      summary: Get a name by its nameId
      description: Get information about the geographical name with the specified
        nameId.
      operationId: get-information-about-the-geographical-name-with-the-specified-nameid-
      x-api-path-slug: namesnameid-outputformat-get
      parameters:
      - in: path
        name: nameId
        description: The unique identifier for a name
      - in: path
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - Names
      - NameId
      - OutputFormat
  /geomarks/copy:
    post:
      summary: Create a new geomark by copying the geometries from one or more existing
        geomarks from the current server.
      description: The source geomarks can be specified by with the geomarkUrl parameter.  Repeat
        the parameter if sourcing from multiple geomarks
      operationId: the-source-geomarks-can-be-specified-by-with-the-geomarkurl-parameter---repeat-the-parameter-if-sour
      x-api-path-slug: geomarkscopy-post
      parameters:
      - in: query
        name: bufferCap
        description: If bufferMetres is specified, The style of buffer to use at the
          ends of a buffered line
      - in: query
        name: bufferJoin
        description: If bufferMetres is specified, The style of buffer to use for
          joins between the line segments for lines and polygons
      - in: query
        name: bufferMetres
        description: The amount to buffer the geometry in metres, must only contain
          numerical digits (e
      - in: query
        name: bufferMitreLimit
        description: If bufferMetres is specified, the maximum ratio of distance from
          the original geometry to a mitre buffer point and the buffer amount
      - in: query
        name: bufferSegments
        description: If bufferMetres is specified, the number of line segments used
          in each quadrant to approximate the curve for round end-cap and join styles
      - in: query
        name: callback
        description: The callback function a JSON result format would be wrapped in
          to support Ajax requests
      - in: query
        name: failureRedirectUrl
        description: The url to redirect if the geomark could not be created
      - in: query
        name: geomarkUrl
        description: One or more geomark URLs or identifiers to create the new geomark
          from
      - in: query
        name: redirectUrl
        description: The optional external URL to redirect the user to when the geomark
          is created rather than showing the geomark info page
      - in: query
        name: resultFormat
        description: The file format the geomark info resource should be returned
          using
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - Copy
  /geomarks/new:
    post:
      summary: Create a new geomark
      description: Create a new geomark from the geometries read from the 'body' parameter
        or file.
      operationId: create-a-new-geomark-from-the-geometries-read-from-the-body-parameter-or-file-
      x-api-path-slug: geomarksnew-post
      parameters:
      - in: formData
        name: body
        description: The binary or character content representing the geometry or
          geometries
      - in: formData
        name: bufferCap
        description: If bufferMetres is specified, The style of buffer to use at the
          ends of a buffered line
      - in: formData
        name: bufferJoin
        description: If bufferMetres is specified, The style of buffer to use for
          joins between the line segments for lines and polygons
      - in: formData
        name: bufferMetres
        description: The amount to buffer the geometry in metres, must only contain
          numerical digits (e
      - in: formData
        name: bufferMitreLimit
        description: If bufferMetres is specified, the maximum ratio of distance from
          the original geometry to a mitre buffer point and the buffer amount
      - in: formData
        name: bufferSegments
        description: If bufferMetres is specified, the number of line segments used
          in each quadrant to approximate the curve for round end-cap and join styles
      - in: formData
        name: callback
        description: The callback function a JSON result format would be wrapped in
          to support Ajax requests
      - in: formData
        name: failureRedirectUrl
        description: The url to redirect if the geomark could not be created
      - in: formData
        name: format
        description: The file format name extension of the input geometry
      - in: formData
        name: multiple
        description: Boolean flag indicating if multiple geometries are to be used
          for the geomark (true) or only a single geometry from the first geometry
          (false)
      - in: formData
        name: redirectUrl
        description: The optional external URL to redirect the user to when the geomark
          is created rather than showing the geomark info page
      - in: formData
        name: resultFormat
        description: The file format the geomark info resource should be returned
          using
      - in: formData
        name: srid
        description: The srid of the coordinate system the input geometries are in
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - New
  /geomarks/{geomarkId}.{fileFormatExtension}:
    get:
      summary: Get information about a particular geomark
      description: The attribution can be downloaded as a info file format. The download
        files can then be processed by a client application to access the geomark
        info fields and to get the URLs to the geometry download resources.
      operationId: the-attribution-can-be-downloaded-as-a-info-file-format--the-download-files-can-then-be-processed-by
      x-api-path-slug: geomarksgeomarkid-fileformatextension-get
      parameters:
      - in: path
        name: fileFormatExtension
        description: The file format name extension used to represent the geomark
          download
      - in: path
        name: geomarkId
        description: The unique identifier for the geomark (e
      - in: query
        name: srid
        description: The srid of the coordinate system the geometry should be converted
          to
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - GeomarkId
      - FileFormatExtension
  /geomarks/{geomarkId}/boundingBox.{fileFormatExtension}:
    get:
      summary: Gets the bounding box of the geomark
      description: The source geomarks can be specified by with the geomarkUrl parameter.  Repeat
        the parameter if sourcing from multiple geomarks
      operationId: the-source-geomarks-can-be-specified-by-with-the-geomarkurl-parameter---repeat-the-parameter-if-sour
      x-api-path-slug: geomarksgeomarkidboundingbox-fileformatextension-get
      parameters:
      - in: path
        name: fileFormatExtension
        description: The file format name extension used to represent the geomark
          download
      - in: path
        name: geomarkId
        description: The unique identifier for the geomark (e
      - in: query
        name: srid
        description: The srid of the coordinate system the geometry should be converted
          to
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - GeomarkId
      - BoundingBox
      - FileFormatExtension
  /geomarks/{geomarkId}/feature.{fileFormatExtension}:
    get:
      summary: Get the feature and attribution of the geomark
      description: The geomark feature resource returns a single spatial feature with
        either a single (Point, LineString, Polygon) or multi-part geometry (MultiPoint,
        MultiLineString, MultiPolygon) and the geomark attribution.  The geometry
        and attribution can be downloaded as a spatial download file format in a supported
        coordinate system. The download files can then be used in a desktop GIS application
        (e.g. ArcMap), Google Earth or a web mapping application.
      operationId: the-geomark-feature-resource-returns-a-single-spatial-feature-with-either-a-single-point-linestring-
      x-api-path-slug: geomarksgeomarkidfeature-fileformatextension-get
      parameters:
      - in: path
        name: fileFormatExtension
        description: The file format name extension used to represent the geomark
          download
      - in: path
        name: geomarkId
        description: The unique identifier for the geomark (e
      - in: query
        name: srid
        description: The srid of the coordinate system the geometry should be converted
          to
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - GeomarkId
      - Feature
      - FileFormatExtension
  /geomarks/{geomarkId}/parts.{fileFormatExtension}:
    get:
      summary: Get the individual geometries within a multi-part geometry
      description: The geomark parts resource returns a one or more spatial features.
        One for each part of the Geomark's geomerty. Each part contains a single (Point,
        LineString, Polygon) geometry and the geomark attribution.
      operationId: the-geomark-parts-resource-returns-a-one-or-more-spatial-features--one-for-each-part-of-the-geomarks
      x-api-path-slug: geomarksgeomarkidparts-fileformatextension-get
      parameters:
      - in: path
        name: fileFormatExtension
        description: The file format name extension used to represent the geomark
          download
      - in: path
        name: geomarkId
        description: The unique identifier for the geomark (e
      - in: query
        name: srid
        description: The srid of the coordinate system the geometry should be converted
          to
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - GeomarkId
      - Parts
      - FileFormatExtension
  /geomarks/{geomarkId}/point.{fileFormatExtension}:
    get:
      summary: Gets a single spatial point representative of the geomark.
      description: The geomark point resource returns a single spatial feature with
        a single Point and the geomark attribution.  The point geometry will be created
        from the first geometry part of the Geomark. Point geomarks will return the
        first Point part in the geomark.  LineString geomarks will return the first
        coordinate of the first LineString part in the geomark. Polygon geomarks will
        return the centroid or another point inside the first Polygon part in the
        geomark. The geometry and attribution can be downloaded as a spatial download
        file format in a supported coordinate system. The download files can then
        be used in a desktop GIS application (e.g. ArcMap), Google Earth or a web
        mapping application.
      operationId: the-geomark-point-resource-returns-a-single-spatial-feature-with-a-single-point-and-the-geomark-attr
      x-api-path-slug: geomarksgeomarkidpoint-fileformatextension-get
      parameters:
      - in: path
        name: fileFormatExtension
        description: The file format name extension used to represent the geomark
          download
      - in: path
        name: geomarkId
        description: The unique identifier for the geomark (e
      - in: query
        name: srid
        description: The srid of the coordinate system the geometry should be converted
          to
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - GeomarkId
      - Point
      - FileFormatExtension