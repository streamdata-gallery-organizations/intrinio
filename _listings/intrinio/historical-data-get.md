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
  /historical_data:
    get:
      summary: Historical Data
      description: Returns the historical data for for a selected identifier (ticker
        symbol or index symbol) for a selected tag
      operationId: historical-data
      parameters:
      - in: query
        name: end_date
        description: ' the latest date for which to return data: YYYY'
        type: string
      - in: query
        name: frequency
        description: ' the frequency of the historical prices &amp; valuation data:
          daily | weekly | monthly | quarterly | yearly'
        type: string
      - in: query
        name: identifier
        description: ' the stock market ticker symbol associated with the company&rsquo;s
          common stock or index'
        type: string
      - in: query
        name: item
        description: ' the specified standardized tag requested'
        type: string
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
        name: sequence
        description: 'in function) '
        type: string
      - in: query
        name: show_date
        description: 'in, false by default) if true, the function will return the
          date value, and if false the function will return the data point value for
          a given query: true | false'
        type: string
      - in: query
        name: sort_order
        description: ' the order of the historical stock price dates: asc | desc'
        type: string
      - in: query
        name: start_date
        description: ' the earliest date for which to return data: YYYY'
        type: string
      - in: query
        name: type
        description: ' the type of periods requested '
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - historical data
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