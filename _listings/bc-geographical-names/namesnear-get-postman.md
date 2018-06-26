{
  "info": {
    "name": "BC Geographical Names Search near to a geographic point",
    "_postman_id": "0e9afcef-47d1-4d68-b02a-a4757bd32761",
    "description": "Search for information about geographical names that correspond to features within a geographic area defined by a centre point and a radius.  Various options and filter parameters are available to refine the search.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "cb5a8b95-e1e1-4566-b451-e81062232f1f",
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
              "id": "cad00879-4ca1-4b25-a421-1044bb61cc8a"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "4d4c902e-c1e7-47c9-b3c6-57a8541901f5",
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
              "id": "fb857b33-f0dd-4916-b7b1-a3283e5b54a6"
            }
          ]
        },
        {
          "id": "a4f31a47-46fb-43d3-9819-2e15ff0522df",
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
              "id": "b3088540-0575-4d03-a999-718d409f5a9b"
            }
          ]
        },
        {
          "id": "84ba0bbd-7fb4-47b4-9a74-aae338b28d12",
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
              "id": "cf719b99-00b0-410e-a34f-fb5cbc7677b8"
            }
          ]
        },
        {
          "id": "86f31f12-1082-4cdf-a31d-7ccc075b7208",
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
              "id": "2b09e030-9970-4734-82e7-debd16cf3c03"
            }
          ]
        },
        {
          "id": "585bed08-e100-4d15-a06d-a05d527cdd4f",
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
              "id": "0367a20c-84a9-4912-99ae-64d9bf5c64c6"
            }
          ]
        }
      ]
    }
  ]
}