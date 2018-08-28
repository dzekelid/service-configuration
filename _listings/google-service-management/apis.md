---
name: Google Service Management
x-slug: google-service-management
description: Google Service Management is an infrastructure service of Google Cloud
  Platform that manages other APIs and services, including Googles own Cloud Platform
  services and their APIs, and services created using Google Cloud Endpoints.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Service Configuration
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/apis.md
specificationVersion: "0.14"
apis:
- name: Google Service Management - Create Service Configuration
  x-api-slug: v1servicesservicenameconfig-get
  description: Gets a service configuration (version) for a managed service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenameconfig-get-openapi.md
- name: Google Service Management - Create Service Configurations
  x-api-slug: v1servicesservicenameconfigs-get
  description: |-
    Lists the history of the service configuration for a managed service,
    from the newest to the oldest.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenameconfigs-get-openapi.md
- name: Google Service Management - Create Service Configuration
  x-api-slug: v1servicesservicenameconfigs-post
  description: |-
    Creates a new service configuration (version) for a managed service.
    This method only stores the service configuration. To roll out the service
    configuration to backend systems please call
    CreateServiceRollout.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenameconfigs-post-openapi.md
- name: Google Service Management - Get Service Configuration
  x-api-slug: v1servicesservicenameconfigsconfigid-get
  description: Gets a service configuration (version) for a managed service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenameconfigsconfigid-get-openapi.md
- name: Google Service Management - Create Service Configuration
  x-api-slug: v1servicesservicenameconfigssubmit-post
  description: |-
    Creates a new service configuration (version) for a managed service based
    on
    user-supplied configuration source files (for example: OpenAPI
    Specification). This method stores the source configurations as well as the
    generated service configuration. To rollout the service configuration to
    other services,
    please call CreateServiceRollout.

    Operation<response: SubmitConfigSourceResponse>
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenameconfigssubmit-post-openapi.md
- name: Google Service Management - Create new Service Configuration
  x-api-slug: v1servicesservicenamerollouts-post
  description: |-
    Creates a new service configuration rollout. Based on rollout, the
    Google Service Management will roll out the service configurations to
    different backend services. For example, the logging configuration will be
    pushed to Google Cloud Logging.

    Please note that any previous pending and running Rollouts and associated
    Operations will be automatically cancelled so that the latest Rollout will
    not be blocked by previous Rollouts.

    Operation<response: Rollout>
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenamerollouts-post-openapi.md
- name: Google Service Management - Get Service Configuration
  x-api-slug: v1servicesservicenamerolloutsrolloutid-get
  description: Gets a service configuration rollout.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-icon.png
  humanURL: https://cloud.google.com/service-management/overview
  baseURL: ://servicemanagement.googleapis.com//
  tags: Management, Google APIs, Stack Network, API Service Provider, API Provider,
    Deployments, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/service-configuration/master/_listings/google-service-management/v1servicesservicenamerolloutsrolloutid-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.service.control.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.service.management.stack.network
- type: x-change-log
  url: https://cloud.google.com/service-management/release-notes
- type: x-code
  url: https://cloud.google.com/service-management/libraries
- type: x-command-line-interface
  url: https://cloud.google.com/sdk/gcloud/reference/beta/service-management/
- type: x-rate-limits
  url: https://cloud.google.com/service-management/quota
- type: x-support
  url: https://cloud.google.com/service-management/support
- type: x-website
  url: https://cloud.google.com/service-management/overview
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---