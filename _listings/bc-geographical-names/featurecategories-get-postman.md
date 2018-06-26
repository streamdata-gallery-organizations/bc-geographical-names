{
  "info": {
    "name": "BC Geographical Names Get all feature categories",
    "_postman_id": "e4e8eda6-d5a4-4ac8-abab-952afc5eaf6a",
    "description": "Gets a list of all feature categories used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "FeatureCategories",
      "item": [
        {
          "id": "6b2f41c6-0a1c-4416-a1c7-68660b411daa",
          "name": "gets-a-list-of-all-feature-categories-used-by-the-bc-geographical-names-information-system-bcgnis---",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/featureCategories?outputFormat=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of all feature categories used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d054792-27fc-4ba4-ad1e-08b34ac1f3dc"
            }
          ]
        }
      ]
    }
  ]
}