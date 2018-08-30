{
  "info": {
    "name": "BC Geographical Names Search in a geographic area",
    "_postman_id": "5e27c560-3160-4210-a3a0-09f7c7a3c34a",
    "description": "Search for information about geographical names that correspond to features within a geographic bounding box.  Various options and filter parameters are available to refine the search.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "3832565b-9db8-428f-845a-1644244bc895",
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
              "id": "623d61c7-7872-4020-9c91-396087f04809"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "45f81551-474b-4ae8-9829-a005322ae79d",
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
              "id": "e601b029-7a82-416b-b4b1-64c1ce0d0463"
            }
          ]
        },
        {
          "id": "0774f639-93d9-43c0-a6f6-f0c4c2660937",
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
              "id": "28be2fb0-dceb-4bda-a288-67fbd0ff2652"
            }
          ]
        },
        {
          "id": "a73680c3-6fb9-4443-806b-06d8bb5c6ff6",
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
              "id": "a28ce616-2ff4-44fe-b298-f4f37391c170"
            }
          ]
        },
        {
          "id": "14a501be-d055-4d78-a745-412ab1390cfd",
          "name": "search-for-information-about-geographical-names-that-correspond-to-features-within-a-geographic-boun",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/inside?bbox=%7B%7D&embed=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names that correspond to features within a geographic bounding box.  Various options and filter parameters are available to refine the search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ece111d-cfee-4d3b-894c-9142a4e0b2a3"
            }
          ]
        }
      ]
    }
  ]
}