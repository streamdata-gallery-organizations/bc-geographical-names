{
  "info": {
    "name": "Geo Mark Web Service Get the individual geometries within a multi-part geometry",
    "_postman_id": "2888fe42-3d86-4222-9dec-6c12e164931b",
    "description": "The geomark parts resource returns a one or more spatial features. One for each part of the Geomark's geomerty. Each part contains a single (Point, LineString, Polygon) geometry and the geomark attribution.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geomarks",
      "item": [
        {
          "id": "e8f30881-d158-496f-a06e-927d34296054",
          "name": "the-source-geomarks-can-be-specified-by-with-the-geomarkurl-parameter---repeat-the-parameter-if-sour",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/geomark/geomarks/copy?bufferCap=%7B%7D&bufferJoin=%7B%7D&bufferMetres=%7B%7D&bufferMitreLimit=%7B%7D&bufferSegments=%7B%7D&callback=%7B%7D&failureRedirectUrl=%7B%7D&geomarkUrl=%7B%7D&redirectUrl=%7B%7D&resultFormat=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "The source geomarks can be specified by with the geomarkUrl parameter.  Repeat the parameter if sourcing from multiple geomarks"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c38616e3-786e-4cd2-bb01-7f6dd66a872a"
            }
          ]
        },
        {
          "id": "bb91e7f6-929e-4def-b5cb-6b0df347f41d",
          "name": "create-a-new-geomark-from-the-geometries-read-from-the-body-parameter-or-file-",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/geomark/geomarks/new",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "body",
                  "value": "{}",
                  "disabled": false,
                  "description": "The binary or character content representing the geometry or geometries"
                },
                {
                  "key": "bufferCap",
                  "value": "{}",
                  "disabled": false,
                  "description": "If bufferMetres is specified, The style of buffer to use at the ends of a buffered line"
                },
                {
                  "key": "bufferJoin",
                  "value": "{}",
                  "disabled": false,
                  "description": "If bufferMetres is specified, The style of buffer to use for joins between the line segments for lines and polygons"
                },
                {
                  "key": "bufferMetres",
                  "value": "{}",
                  "disabled": false,
                  "description": "The amount to buffer the geometry in metres, must only contain numerical digits (e"
                },
                {
                  "key": "bufferMitreLimit",
                  "value": "{}",
                  "disabled": false,
                  "description": "If bufferMetres is specified, the maximum ratio of distance from the original geometry to a mitre buffer point and the buffer amount"
                },
                {
                  "key": "bufferSegments",
                  "value": "{}",
                  "disabled": false,
                  "description": "If bufferMetres is specified, the number of line segments used in each quadrant to approximate the curve for round end-cap and join styles"
                },
                {
                  "key": "callback",
                  "value": "{}",
                  "disabled": false,
                  "description": "The callback function a JSON result format would be wrapped in to support Ajax requests"
                },
                {
                  "key": "failureRedirectUrl",
                  "value": "{}",
                  "disabled": false,
                  "description": "The url to redirect if the geomark could not be created"
                },
                {
                  "key": "format",
                  "value": "{}",
                  "disabled": false,
                  "description": "The file format name extension of the input geometry"
                },
                {
                  "key": "multiple",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean flag indicating if multiple geometries are to be used for the geomark (true) or only a single geometry from the first geometry (false)"
                },
                {
                  "key": "redirectUrl",
                  "value": "{}",
                  "disabled": false,
                  "description": "The optional external URL to redirect the user to when the geomark is created rather than showing the geomark info page"
                },
                {
                  "key": "resultFormat",
                  "value": "{}",
                  "disabled": false,
                  "description": "The file format the geomark info resource should be returned using"
                },
                {
                  "key": "srid",
                  "value": "{}",
                  "disabled": false,
                  "description": "The srid of the coordinate system the input geometries are in"
                }
              ]
            },
            "description": "Create a new geomark from the geometries read from the 'body' parameter or file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "03b8bfd7-c629-4c77-b133-3a8ae68ad885"
            }
          ]
        },
        {
          "id": "a91ee38f-c91b-415d-9586-5b9d3f55165f",
          "name": "the-attribution-can-be-downloaded-as-a-info-file-format--the-download-files-can-then-be-processed-by",
          "request": {
            "url": {
              "protocol": "http",
              "host": "apps.gov.bc.ca",
              "path": [
                "pub",
                "geomark",
                "geomarks/:geomarkId.:fileFormatExtension"
              ],
              "query": [
                {
                  "key": "srid",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fileFormatExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "geomarkId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The attribution can be downloaded as a info file format. The download files can then be processed by a client application to access the geomark info fields and to get the URLs to the geometry download resources."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "982c71bc-bfc0-45ac-87ba-94fb45d4b6a0"
            }
          ]
        },
        {
          "id": "e8f95603-97d5-467c-ab4e-230c9cb4c943",
          "name": "the-source-geomarks-can-be-specified-by-with-the-geomarkurl-parameter---repeat-the-parameter-if-sour",
          "request": {
            "url": {
              "protocol": "http",
              "host": "apps.gov.bc.ca",
              "path": [
                "pub",
                "geomark",
                "geomarks/:geomarkId/boundingBox.:fileFormatExtension"
              ],
              "query": [
                {
                  "key": "srid",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fileFormatExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "geomarkId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The source geomarks can be specified by with the geomarkUrl parameter.  Repeat the parameter if sourcing from multiple geomarks"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f80ae285-9dfc-422c-b790-a169613aaf5f"
            }
          ]
        },
        {
          "id": "eef9f079-711e-4c61-b4b2-a3339a353b10",
          "name": "the-geomark-feature-resource-returns-a-single-spatial-feature-with-either-a-single-point-linestring-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "apps.gov.bc.ca",
              "path": [
                "pub",
                "geomark",
                "geomarks/:geomarkId/feature.:fileFormatExtension"
              ],
              "query": [
                {
                  "key": "srid",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fileFormatExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "geomarkId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The geomark feature resource returns a single spatial feature with either a single (Point, LineString, Polygon) or multi-part geometry (MultiPoint, MultiLineString, MultiPolygon) and the geomark attribution.  The geometry and attribution can be downloaded as a spatial download file format in a supported coordinate system. The download files can then be used in a desktop GIS application (e.g. ArcMap), Google Earth or a web mapping application."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13c64fe9-784e-4d61-88d1-0f0a60f5ea69"
            }
          ]
        },
        {
          "id": "68a2f64e-0411-4d8a-8d8b-b640842002c8",
          "name": "the-geomark-parts-resource-returns-a-one-or-more-spatial-features--one-for-each-part-of-the-geomarks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "apps.gov.bc.ca",
              "path": [
                "pub",
                "geomark",
                "geomarks/:geomarkId/parts.:fileFormatExtension"
              ],
              "query": [
                {
                  "key": "srid",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fileFormatExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "geomarkId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The geomark parts resource returns a one or more spatial features. One for each part of the Geomark's geomerty. Each part contains a single (Point, LineString, Polygon) geometry and the geomark attribution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7533dd78-92c7-4136-a95f-d97bc17788a9"
            }
          ]
        }
      ]
    }
  ]
}