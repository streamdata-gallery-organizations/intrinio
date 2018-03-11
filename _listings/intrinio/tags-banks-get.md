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
  /tags/banks:
    get:
      summary: Bank XBRL Tags and Labels
      description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID,
        statement, and date or fiscal year/fiscal quarter
      operationId: bank-xbrl-tags-and-labels
      parameters:
      - in: query
        name: fiscal_period
        description: ' the fiscal period associated with the fundamental: FY | Q1
          | Q2 | Q3 | Q4 | Q1TTM | Q2TTM | Q3TTM | Q2YTD | Q3YTD'
        type: string
      - in: query
        name: fiscal_year
        description: ' the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: ' the stock market ticker symbol associated with the companies
          common stock securities, or the bank/bank holding company RSSD ID issued
          by the Federal Reserve: '
        type: string
      - in: query
        name: item
        description: 'in function) '
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
        description: ' an integer 0 or greater for calling a single tag from the first
          entry'
        type: string
      - in: query
        name: statement
        description: ' the financial statement requested from the call report, the
          UBPR report or Y'
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - banks
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