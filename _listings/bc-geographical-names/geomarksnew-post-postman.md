{
  "info": {
    "name": "Geo Mark Web Service Create a new geomark",
    "_postman_id": "74680b9c-5d8b-417c-b9e9-fd615f005d3a",
    "description": "Create a new geomark from the geometries read from the 'body' parameter or file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geomarks",
      "item": [
        {
          "id": "9312275f-f620-40a1-a6fa-cd3ab91861f7",
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
              "id": "8520caf6-1576-49bf-8d86-a9675f18a99a"
            }
          ]
        },
        {
          "id": "499665d2-93fb-4531-965f-106e678bb62f",
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
              "id": "30287b82-1f98-434e-b662-76501e434483"
            }
          ]
        }
      ]
    }
  ]
}