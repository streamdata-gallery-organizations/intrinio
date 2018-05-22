---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 0
info:
  title: Intrinio API Stock Exchange Master
  description: Returns stock exchange list and information for all stock exchanges
    covered by Intrinio.
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
  /companies:
    get:
      summary: Company Master
      description: Returns the master list of all companies covered by the Intrinio
        Data Marketplace.  You can view the Company/Security Master here.
      operationId: company-master
      x-api-path-slug: companies-get
      parameters:
      - in: query
        name: latest_filing_date
        description: ' a date value that returns the list of companies whose latest
          SEC filing was filed on or after this date: YYYY'
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
        name: query
        description: ' a string query search of company name or ticker symbol with
          the returned results being the relevant companies in compacted list format'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Companies
  /indices:
    get:
      summary: Index Master
      description: 'Returns indices list and information for all indices covered by
        Intrinio. There are three distinct types of indices: Stock Market, SIC (Sector
        &amp; Industry), and Economic.  You can view the Stock Market Indices Master,
        SIC Indices Master, and the Economic Indices Master.'
      operationId: index-master
      x-api-path-slug: indices-get
      parameters:
      - in: query
        name: identifier
        description: ' the Intrinio symbol associated with the index: '
        type: string
      - in: query
        name: order
        description: ' returns the results in the given order: popularity | symbol'
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
        name: query
        description: ' a string query search of index name or symbol with the returned
          results being the relevant securities in compacted list format'
        type: string
      - in: query
        name: type
        description: ' the type of indices specified: stock_market | economic | sic'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Indices
  /stock_exchanges:
    get:
      summary: Stock Exchange Master
      description: Returns stock exchange list and information for all stock exchanges
        covered by Intrinio.
      operationId: stock-exchange-master
      x-api-path-slug: stock-exchanges-get
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
        name: query
        description: ' a string query search of stock exchange name or MIC with the
          returned results being the relevant stock exchanges in compacted list format'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Stock Exchanges
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