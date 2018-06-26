---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: Geo Mark Web Service Create a new geomark by copying the geometries from
    one or more existing geomarks from the current server.
  description: The source geomarks can be specified by with the geomarkUrl parameter.  Repeat
    the parameter if sourcing from multiple geomarks
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