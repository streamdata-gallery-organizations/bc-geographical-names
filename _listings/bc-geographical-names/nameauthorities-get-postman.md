{
  "info": {
    "name": "BC Geographical Names Get all name authorities",
    "_postman_id": "0f6d271b-1eb6-4b7e-9f6d-668bea59308c",
    "description": "Gets a list of all name authorities responsible for naming decisions of the geographical names in the BC Geographical Names Information System (BCGNIS)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "NameAuthorities",
      "item": [
        {
          "id": "398e4349-d26c-4ad2-ac31-e8598f50db21",
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
              "id": "754b99fe-a8af-48ec-b28f-353a66e4b3e4"
            }
          ]
        }
      ]
    }
  ]
}