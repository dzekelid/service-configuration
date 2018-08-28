---
swagger: "2.0"
x-collection-name: Google Service Management
x-complete: 0
info:
  title: Google Service Management API Create Service Configuration
  description: Gets a service configuration (version) for a managed service.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: servicemanagement.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/services/{serviceName}/config:
    get:
      summary: Create Service Configuration
      description: Gets a service configuration (version) for a managed service.
      operationId: servicemanagement.services.getConfig
      x-api-path-slug: v1servicesservicenameconfig-get
      parameters:
      - in: query
        name: configId
        description: The id of the service configuration resource
      - in: path
        name: serviceName
        description: The name of the service
      - in: query
        name: view
        description: Specifies which parts of the Service Config should be returned
          in theresponse
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
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