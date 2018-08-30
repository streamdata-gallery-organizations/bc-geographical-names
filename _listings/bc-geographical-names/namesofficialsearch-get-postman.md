{
  "info": {
    "name": "BC Geographical Names Search by name, limit to official names only",
    "_postman_id": "134b2fd9-c2cf-4ad3-9871-e85407ba9ca1",
    "description": "Search for information about official geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "4c356803-ff75-48e4-a03a-eb2b42452336",
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
              "id": "82fa4650-27a4-4ddd-becc-e47fea84edf8"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "4e54ffd4-fe9f-4f99-b62f-6477cbc2f767",
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
              "id": "23525978-930d-452a-bcbe-fdf3aa0a26c6"
            }
          ]
        },
        {
          "id": "18f88fd9-572b-42f9-a365-b4c677827d29",
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
              "id": "1b48fc40-d2bc-464f-b669-2cdd8aed8a54"
            }
          ]
        },
        {
          "id": "72c122a1-1e2f-420d-9b81-211427742dfc",
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
              "id": "a9a70478-4d14-45bf-935c-a351dc55dd2a"
            }
          ]
        },
        {
          "id": "06f432f3-f649-46c3-b857-b1fae29ea19a",
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
              "id": "b5f8d697-27ee-4065-839b-71604208340e"
            }
          ]
        },
        {
          "id": "2faa2c35-08de-4c6e-8f6d-f875bffb900c",
          "name": "search-for-information-about-geographical-names-that-correspond-to-features-within-a-geographic-area",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/near?distance=%7B%7D&embed=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featurePoint=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names that correspond to features within a geographic area defined by a centre point and a radius.  Various options and filter parameters are available to refine the search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ed8edca-c388-4983-9453-8047086f3eb3"
            }
          ]
        },
        {
          "id": "21434ce2-40f1-4d1a-85ca-f4a6c5378eb5",
          "name": "search-for-information-about-unofficial-geographical-names-by-the-text-of-the-name-itself---various-",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/notOfficial/search?embed=%7B%7D&exactSpelling=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&name=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about unofficial geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1023aedb-4641-4235-ab7c-d632b69c0cf1"
            }
          ]
        },
        {
          "id": "f978b6e3-8998-4cba-9ca6-657ffefc4e98",
          "name": "search-for-information-about-official-geographical-names-by-the-text-of-the-name-itself---various-op",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/official/search?embed=%7B%7D&exactSpelling=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&name=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about official geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b57145a-60bc-4281-8a62-ed00a3eec928"
            }
          ]
        }
      ]
    }
  ]
}