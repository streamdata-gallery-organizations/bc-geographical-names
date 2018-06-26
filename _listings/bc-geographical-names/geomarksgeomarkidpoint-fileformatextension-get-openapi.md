---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: Geo Mark Web Service Gets a single spatial point representative of the geomark.
  description: The geomark point resource returns a single spatial feature with a
    single Point and the geomark attribution.  The point geometry will be created
    from the first geometry part of the Geomark. Point geomarks will return the first
    Point part in the geomark.  LineString geomarks will return the first coordinate
    of the first LineString part in the geomark. Polygon geomarks will return the
    centroid or another point inside the first Polygon part in the geomark. The geometry
    and attribution can be downloaded as a spatial download file format in a supported
    coordinate system. The download files can then be used in a desktop GIS application
    (e.g. ArcMap), Google Earth or a web mapping application.
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