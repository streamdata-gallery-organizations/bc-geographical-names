{
  "info": {
    "name": "BC Geographical Names Get all feature classes",
    "_postman_id": "4eded68c-7a9d-4e28-9a1f-906e14742766",
    "description": "Gets a list of all feature classes used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "FeatureClasses",
      "item": [
        {
          "id": "2b7d9110-0fce-422f-a130-271aa547eb98",
          "name": "gets-a-list-of-all-feature-classes-used-by-the-bc-geographical-names-information-system-bcgnis---not",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/featureClasses?outputFormat=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of all feature classes used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2a6a7077-6b6e-4ee9-b2aa-ef4aa37363fc"
            }
          ]
        }
      ]
    }
  ]
}