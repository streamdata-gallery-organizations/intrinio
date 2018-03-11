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
  /analysts:
    get:
      summary: Analysts
      description: Returns a list of analysts
      operationId: analysts
      parameters:
      - in: query
        name: page_number
        description: ' an integer greater than or equal to 1 for specifying the page
          number for the return values'
        type: string
      - in: query
        name: page_size
        description: ' an integer greater than 1 for specifying the number of results
          on each page'
        type: string
      - in: query
        name: source
        description: ' The source of the data: tip'
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - analysts
definitions: []
x-collection-name: Intrinio
x-streamrank:
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: ~
  last_run: ~
  days_run: ~
  minute_run: ~
---