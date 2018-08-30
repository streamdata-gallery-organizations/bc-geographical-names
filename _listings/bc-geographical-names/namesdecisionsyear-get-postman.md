{
  "info": {
    "name": "BC Geographical Names Search for names affected by naming decisions in a given year",
    "_postman_id": "9028fbd7-e0db-45b5-b256-27cc92e45bfd",
    "description": "Search for information about geographical names affected by naming 'decisions' made by the BC Geographical Names Office (naming authority) in a given year.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "7ce5d53b-e491-407c-b97a-c9f76b21c458",
          "name": "gets-a-list-of-all-name-authorities-responsible-for-naming-decisions-of-the-geographical-names-in-th",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/nameAuthorities?outputFormat=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of all name authorities responsible for naming decisions of the geographical names in the BC Geographical Names Information System (BCGNIS)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57857c30-c136-4c66-9be6-c7f74436dc5e"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "24911b60-60b6-4496-b73f-ce24ff64c191",
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
              "id": "ed927524-74c4-4ccb-8b48-94561897d072"
            }
          ]
        },
        {
          "id": "b8376243-4876-4d10-ad3b-97a102eb2d54",
          "name": "search-for-information-about-geographical-names-affected-by-naming-decisions-made-by-the-bc-geograph",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/decisions/recent?days=%7B%7D&embed=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names affected by naming 'decisions' made by the BC Geographical Names Office (naming authority) within the last X days."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31cf36ce-96c2-4a99-a10d-f4d29b401db3"
            }
          ]
        },
        {
          "id": "506022df-9d65-48fd-8ffd-1e018f4c9b80",
          "name": "search-for-information-about-geographical-names-affected-by-naming-decisions-made-by-the-bc-geograph",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/decisions/year?embed=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D&year=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names affected by naming 'decisions' made by the BC Geographical Names Office (naming authority) in a given year."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8364ead1-60b6-4418-9d82-af1fa84c005b"
            }
          ]
        }
      ]
    }
  ]
}