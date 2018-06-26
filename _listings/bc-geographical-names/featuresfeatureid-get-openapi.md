---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: BC Geographical Names Get a feature by its featureId
  description: Get information about the geographical feature with the specified featureId.
  contact:
    name: BC Geographical Names Office
    email: geographical.names@gov.bc.ca
  version: 3.x.x
host: apps.gov.bc.ca
basePath: /pub/bcgnws
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /featureCategories:
    get:
      summary: Get all feature categories
      description: 'Gets a list of all feature categories used by the BC Geographical
        Names Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-categories-used-by-the-bc-geographical-names-information-system-bcgnis---
      x-api-path-slug: featurecategories-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureCategories
  /featureClasses:
    get:
      summary: Get all feature classes
      description: 'Gets a list of all feature classes used by the BC Geographical
        Names Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-classes-used-by-the-bc-geographical-names-information-system-bcgnis---not
      x-api-path-slug: featureclasses-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureClasses
  /featureTypes:
    get:
      summary: Get all feature types
      description: 'Gets a list of all feature types used by the BC Geographical Names
        Information System (BCGNIS).  Note: there are three levels of classification
        in the BCGNIS feature taxonomy: classes, categories and types.  A type is
        a subset of a category, and a category is a subset of a class.'
      operationId: gets-a-list-of-all-feature-types-used-by-the-bc-geographical-names-information-system-bcgnis---note-
      x-api-path-slug: featuretypes-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - FeatureTypes
  /features/{featureId}:
    get:
      summary: Get a feature by its featureId
      description: Get information about the geographical feature with the specified
        featureId.
      operationId: get-information-about-the-geographical-feature-with-the-specified-featureid-
      x-api-path-slug: featuresfeatureid-get
      parameters:
      - in: path
        name: featureId
        description: The unique identifier for a feature
      responses:
        200:
          description: OK
      tags:
      - Features
      - FeatureId
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---