{
  "info": {
    "name": "BC Geographical Names Get a feature by its featureId",
    "_postman_id": "52141833-9db0-40f8-80fa-fa75a9bceb11",
    "description": "Get information about the geographical feature with the specified featureId.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "FeatureCategories",
      "item": [
        {
          "id": "220bcceb-0ec2-4bcb-a3f0-9fa53e5d744b",
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
              "id": "56dd364d-1662-4836-a1b9-019d966e7490"
            }
          ]
        }
      ]
    },
    {
      "name": "FeatureClasses",
      "item": [
        {
          "id": "89483250-adca-4482-9c8c-57e2a99805af",
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
              "id": "a4a4abb9-39b6-499d-a614-11b1cb05fccb"
            }
          ]
        }
      ]
    },
    {
      "name": "FeatureTypes",
      "item": [
        {
          "id": "eade6837-7073-4209-a01a-62592b8d3ac9",
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
              "id": "b7d76e8f-f25d-4e90-8399-6811ffa0d088"
            }
          ]
        }
      ]
    },
    {
      "name": "Features",
      "item": [
        {
          "id": "74e7463d-f30f-4211-af80-eb38bef7fc66",
          "name": "get-information-about-the-geographical-feature-with-the-specified-featureid-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "apps.gov.bc.ca",
              "path": [
                "pub",
                "bcgnws",
                "features/:featureId"
              ],
              "variable": [
                {
                  "id": "featureId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about the geographical feature with the specified featureId."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "93cc2753-212e-4d25-bc5e-a6b4b255c524"
            }
          ]
        }
      ]
    }
  ]
}