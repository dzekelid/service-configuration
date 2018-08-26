---
swagger: "2.0"
x-collection-name: Google Service Management
x-complete: 1
info:
  title: Google Service Management
  description: google-service-management-allows-service-producers-to-publish-their-services-on-google-cloud-platform-so-that-they-can-be-discovered-and-used-by-service-consumers-
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
  /v1/services/{serviceName}/configs:
    get:
      summary: Create Service Configurations
      description: |-
        Lists the history of the service configuration for a managed service,
        from the newest to the oldest.
      operationId: servicemanagement.services.configs.list
      x-api-path-slug: v1servicesservicenameconfigs-get
      parameters:
      - in: query
        name: pageSize
        description: The max number of items to include in the response list
      - in: query
        name: pageToken
        description: The token of the page to retrieve
      - in: path
        name: serviceName
        description: The name of the service
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
    post:
      summary: Create Service Configuration
      description: |-
        Creates a new service configuration (version) for a managed service.
        This method only stores the service configuration. To roll out the service
        configuration to backend systems please call
        CreateServiceRollout.
      operationId: servicemanagement.services.configs.create
      x-api-path-slug: v1servicesservicenameconfigs-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: serviceName
        description: The name of the service
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
  /v1/services/{serviceName}/configs/{configId}:
    get:
      summary: Get Service Configuration
      description: Gets a service configuration (version) for a managed service.
      operationId: servicemanagement.services.configs.get
      x-api-path-slug: v1servicesservicenameconfigsconfigid-get
      parameters:
      - in: path
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
  /v1/services/{serviceName}/configs:submit:
    post:
      summary: Create Service Configuration
      description: |-
        Creates a new service configuration (version) for a managed service based
        on
        user-supplied configuration source files (for example: OpenAPI
        Specification). This method stores the source configurations as well as the
        generated service configuration. To rollout the service configuration to
        other services,
        please call CreateServiceRollout.

        Operation<response: SubmitConfigSourceResponse>
      operationId: servicemanagement.services.configs.submit
      x-api-path-slug: v1servicesservicenameconfigssubmit-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: serviceName
        description: The name of the service
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
  /v1/services/{serviceName}/rollouts:
    post:
      summary: Create new Service Configuration
      description: |-
        Creates a new service configuration rollout. Based on rollout, the
        Google Service Management will roll out the service configurations to
        different backend services. For example, the logging configuration will be
        pushed to Google Cloud Logging.

        Please note that any previous pending and running Rollouts and associated
        Operations will be automatically cancelled so that the latest Rollout will
        not be blocked by previous Rollouts.

        Operation<response: Rollout>
      operationId: servicemanagement.services.rollouts.create
      x-api-path-slug: v1servicesservicenamerollouts-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: serviceName
        description: The name of the service
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
  /v1/services/{serviceName}/rollouts/{rolloutId}:
    get:
      summary: Get Service Configuration
      description: Gets a service configuration rollout.
      operationId: servicemanagement.services.rollouts.get
      x-api-path-slug: v1servicesservicenamerolloutsrolloutid-get
      parameters:
      - in: path
        name: rolloutId
        description: The id of the rollout resource
      - in: path
        name: serviceName
        description: The name of the service
      responses:
        200:
          description: OK
      tags:
      - Service Configuration
---