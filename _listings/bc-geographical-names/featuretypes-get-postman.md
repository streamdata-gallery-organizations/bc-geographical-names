{
  "info": {
    "name": "BC Geographical Names Get all feature types",
    "_postman_id": "aeb58e2f-af82-4bc8-b968-f89b611949ec",
    "description": "Gets a list of all feature types used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "FeatureTypes",
      "item": [
        {
          "id": "d42fb886-fefa-4f5d-a1b8-71ec2cbc82fe",
          "name": "gets-a-list-of-all-feature-types-used-by-the-bc-geographical-names-information-system-bcgnis---note-",
          "request": {
            "url": "http://apps.gov.bc.ca/pub/bcgnws/featureTypes?outputFormat=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of all feature types used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b354bcd3-a3a6-4a8e-b3b5-f28da450c578"
            }
          ]
        }
      ]
    }
  ]
}