---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: BC Geographical Names Get all feature categories
  description: 'Gets a list of all feature categories used by the BC Geographical
    Names Information System (BCGNIS).  Note: there are three levels of classification
    in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset
    of a category, and a category is a subset of a class.'
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