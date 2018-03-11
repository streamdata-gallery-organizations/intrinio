---
swagger: "2.0"
info:
  title: Intrinio
  description: Through our Intrinio Data Marketplace, we offer a wide selection of
    financial data feeds sourced by our own proprietary processes as well as from
    many data vendors. The primary application of the Intrinio API is for use in third-party
    applications and integrations or for end-users utilizing the Excel add-in and
    Google Sheets add-on. The Intrinio API uses HTTPS verbs and a RESTful endpoint
    structure, which makes it easy to request data from Intrinio. Basic Authentication
    is administered over HTTPS. Responses are delivered in JSON format.
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /securities/search:
    get:
      summary: Securities Search/Screener
      description: Returns a list of all securities that match the given conditions
      operationId: securities-searchscreener
      parameters:
      - in: query
        name: |-
          An operator


            Equal to: &ldquo;eq&rdquo;
        type: string
      - in: query
        name: conditions
        description: ' A comma'
        type: string
      - in: query
        name: 'Contains text: &ldquo;contains&rdquo;'
        type: string
      - in: query
        name: 'Greater than or equal to: &ldquo;gte&rdquo;'
        type: string
      - in: query
        name: 'Greater than: &ldquo;gt&rdquo;'
        type: string
      - in: query
        name: 'Less than or equal to: &ldquo;lte&rdquo;'
        type: string
      - in: query
        name: 'Less than: &ldquo;lt&rdquo;'
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - securities
definitions: []
x-collection-name: Intrinio
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