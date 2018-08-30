{
  "info": {
    "name": "BC Geographical Names Search by name, limit to unofficial names only",
    "_postman_id": "911b7e3a-0df0-4dca-b878-204625bcd9ac",
    "description": "Search for information about unofficial geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "049dc85d-3294-4ca0-8a41-29cbc4ec1184",
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
              "id": "cd224a7d-fc66-4c57-bacf-3267a990338c"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "01facb56-cfcf-40db-996d-654158e9471b",
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
              "id": "469af245-c658-4ade-a21b-8a99e90726ad"
            }
          ]
        },
        {
          "id": "e33d7441-cbf9-4cc4-be93-4cb3b6ae216c",
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
              "id": "b6755ad4-2771-4a2c-8e66-4268de42a1ed"
            }
          ]
        },
        {
          "id": "01322a5c-f255-425c-acba-1828c722a955",
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
              "id": "8c974c64-e609-41b7-a237-8cd52ff4eae8"
            }
          ]
        },
        {
          "id": "5466aaa5-eff8-4939-a47d-5753b86db3ef",
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
              "id": "bbf05a62-4374-4f1c-8bc4-ee382e57663e"
            }
          ]
        },
        {
          "id": "8c20fdb8-fb83-43e1-985a-e00d7c5dbf72",
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
              "id": "7cc210f9-d753-436e-92cc-7ad81f1db422"
            }
          ]
        },
        {
          "id": "a8142f42-70fc-4e21-bafc-1bf51a978a14",
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
              "id": "74d1c26a-cbd5-4d24-bb56-dac0f787221f"
            }
          ]
        }
      ]
    }
  ]
}