{
  "info": {
    "name": "Geo Mark Web Service Get information about a particular geomark",
    "_postman_id": "f62f5a25-7fe9-4abb-adc2-ce17d16066ce",
    "description": "The attribution can be downloaded as a info file format. The download files can then be processed by a client application to access the geomark info fields and to get the URLs to the geometry download resources.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geomarks",
      "item": [
        {
          "id": "89dd98de-ee1f-4d4f-9d8b-7d88d18f2cee",
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
              "id": "6b4ac6b8-7eb2-4a33-8c59-7ce86d8ea14c"
            }
          ]
        },
        {
          "id": "d2b89ca0-8344-4cdd-8714-2dc8d88dfe25",
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
              "id": "a6dfbb17-5905-4781-a788-21f3e6a5fc67"
            }
          ]
        },
        {
          "id": "a7a69288-19e0-4833-9b8a-4fea8ded4bfd",
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
              "id": "a10ee585-c0a2-4aad-82e0-07d0384ea0d5"
            }
          ]
        }
      ]
    }
  ]
}