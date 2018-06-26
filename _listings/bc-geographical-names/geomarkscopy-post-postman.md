{
  "info": {
    "name": "Geo Mark Web Service Create a new geomark by copying the geometries from one or more existing geomarks from the current server.",
    "_postman_id": "b13cf571-3aa0-4d43-a735-2081ef5ca45f",
    "description": "The source geomarks can be specified by with the geomarkUrl parameter.  Repeat the parameter if sourcing from multiple geomarks",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geomarks",
      "item": [
        {
          "id": "71d7a670-aeeb-42f0-8200-046b68dacc68",
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
              "id": "8e0ee4de-bf92-4402-8703-04585a6d75ab"
            }
          ]
        }
      ]
    }
  ]
}