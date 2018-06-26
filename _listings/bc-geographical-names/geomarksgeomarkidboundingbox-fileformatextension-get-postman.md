{
  "info": {
    "name": "Geo Mark Web Service Gets the bounding box of the geomark",
    "_postman_id": "063431dc-97bc-44e6-8d06-72c2491913e6",
    "description": "The source geomarks can be specified by with the geomarkUrl parameter.  Repeat the parameter if sourcing from multiple geomarks",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geomarks",
      "item": [
        {
          "id": "54acfa33-8c71-4f88-aa44-ad4d4f8516b2",
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
              "id": "46d6b89b-6c45-4ca5-94c4-50601e6ef5a3"
            }
          ]
        },
        {
          "id": "6270931e-5c12-4f7c-9e0e-6854debc894c",
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
              "id": "05f7d693-ec02-4054-bf30-b12f0b2b97bb"
            }
          ]
        },
        {
          "id": "02bb1d5f-f211-43b9-823d-b332e5508fe7",
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
              "id": "dd971e52-a96d-450e-a23a-397ef47694ab"
            }
          ]
        },
        {
          "id": "f35c3e3c-09d4-4133-bcdc-09e730d8b05f",
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
              "id": "be3e67c6-da4d-44e8-a7f0-ae5d040fccc7"
            }
          ]
        }
      ]
    }
  ]
}