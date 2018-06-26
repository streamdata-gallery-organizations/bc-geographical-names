{
  "info": {
    "name": "BC Geographical Names Search by name",
    "_postman_id": "29bc9523-1a8c-46e6-bba2-a1faeff0fb28",
    "description": "Search for information about geographical names by the text of the name itself.  The response will include both official and unofficial names.  Various options and filter parameters are available to refine the search.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "ca5eead3-8730-4ece-bb3e-9d416e83f87d",
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
              "id": "f2a587b3-345f-4db3-bed1-644fa73ab62e"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "53036d07-8395-4641-a61d-1dacf6f94487",
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
              "id": "dea7a383-8f2d-43f5-a87f-d5c5dc2ba1bc"
            }
          ]
        },
        {
          "id": "5c6487ae-9d24-4740-8f2d-0fe8acd1929b",
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
              "id": "f2dbd4e9-9c04-4c97-b933-d1d4578d7be6"
            }
          ]
        },
        {
          "id": "56069783-8c08-48cf-a325-c7afb1bf8abf",
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
              "id": "faa7c133-d24d-4909-8c57-3e20b9f1b0c2"
            }
          ]
        },
        {
          "id": "d791e902-9a78-451c-ad4b-e9db8941af33",
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
              "id": "db6c6871-e604-4046-9818-999fc53823a1"
            }
          ]
        },
        {
          "id": "a41284ad-427c-4bfd-8d2d-f1114b2c810a",
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
              "id": "b18d0962-1ce2-4b2f-aadd-3eca891b4169"
            }
          ]
        },
        {
          "id": "0e85c5f4-8e5d-4f97-b624-d240d1647921",
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
              "id": "bf18d8c4-85dc-4913-a6ca-c5967469bf97"
            }
          ]
        },
        {
          "id": "9bd0fc6d-eb31-4553-bb13-5c1e65b2df23",
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
              "id": "9118602b-0b24-4e40-9016-8c1a8a0fb30e"
            }
          ]
        },
        {
          "id": "25c424f6-f833-4e94-8b15-8338bb4cc5d6",
          "name": "search-for-information-about-geographical-names-by-the-text-of-the-name-itself---the-response-will-i",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/names/search?embed=%7B%7D&exactSpelling=%7B%7D&featureCategory=%7B%7D&featureClass=%7B%7D&featureType=%7B%7D&itemsPerPage=%7B%7D&name=%7B%7D&outputFormat=%7B%7D&outputSRS=%7B%7D&outputStyle=%7B%7D&sortBy=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for information about geographical names by the text of the name itself.  The response will include both official and unofficial names.  Various options and filter parameters are available to refine the search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e591b01-0474-404b-9ad5-5dccbb92783f"
            }
          ]
        }
      ]
    }
  ]
}