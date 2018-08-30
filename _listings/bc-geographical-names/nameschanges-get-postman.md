{
  "info": {
    "name": "BC Geographical Names Search for names with metadata changes in a given period",
    "_postman_id": "d5573df0-a804-4d9b-ae11-09cc8f5027ce",
    "description": "Search for information about geographical names which have changed most recently within a specified time window.  Changes may include status cupdates and metadata corrections.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Names",
      "item": [
        {
          "id": "14727f25-bf5e-4777-86f1-dd69a7685e58",
          "name": "search-for-information-about-geographical-names-which-have-changed-most-recently-within-a-specified-",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/changes?embed=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&fromDate=%7B%7D&itemsPerPage=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D&toDate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names which have changed most recently within a specified time window.  Changes may include status cupdates and metadata corrections."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d78e883e-8a6b-4bc0-82d3-af678c05f87f"
            }
          ]
        }
      ]
    }
  ]
}