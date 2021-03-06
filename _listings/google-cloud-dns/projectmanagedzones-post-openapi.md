---
swagger: "2.0"
x-collection-name: Google Cloud DNS
x-complete: 0
info:
  title: Google Cloud DNS API Create Managed Zone
  description: Create a new ManagedZone.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /dns/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/managedZones:
    get:
      summary: Get Managed Zones
      description: Enumerate ManagedZones that have been created but not yet deleted.
      operationId: dns.managedZones.list
      x-api-path-slug: projectmanagedzones-get
      parameters:
      - in: query
        name: dnsName
        description: Restricts the list to return only zones with this domain name
      - in: query
        name: maxResults
        description: Optional
      - in: query
        name: pageToken
        description: Optional
      - in: path
        name: project
        description: Identifies the project addressed by this request
      responses:
        200:
          description: OK
      tags:
      - Managed Zone
    post:
      summary: Create Managed Zone
      description: Create a new ManagedZone.
      operationId: dns.managedZones.create
      x-api-path-slug: projectmanagedzones-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Identifies the project addressed by this request
      responses:
        200:
          description: OK
      tags:
      - Managed Zone
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