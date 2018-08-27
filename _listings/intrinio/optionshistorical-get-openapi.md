---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 0
info:
  title: Intrinio API Historical Prices
  description: Returns the historical prices for the given option contract.
  version: 1.0.0
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
        description: 'a date value that returns the list of companies whose latest
          SEC filing was filed on or after this date: YYYY'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of company name or ticker symbol with the
          returned results being the relevant companies in compacted list format
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
        description: 'the Intrinio symbol associated with the index:'
        type: string
      - in: query
        name: order
        description: 'returns the results in the given order: popularity | symbol'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of index name or symbol with the returned
          results being the relevant securities in compacted list format
        type: string
      - in: query
        name: type
        description: 'the type of indices specified: stock_market | economic | sic'
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
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of stock exchange name or MIC with the
          returned results being the relevant stock exchanges in compacted list format
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Stock Exchanges
  /securities:
    get:
      summary: Securities
      description: Returns security list and information for all securities covered
        by Intrinio.
      operationId: securities
      x-api-path-slug: securities-get
      parameters:
      - in: query
        name: exch_symbol
        description: 'the Intrinio Stock Market Symbol, to specify the exchange for
          the list of securities:'
        type: string
      - in: query
        name: identifier
        description: 'the identifier for the legal entity or a security associated
          with the company:'
        type: string
      - in: query
        name: last_crsp_adj_date
        description: 'a date value that returns the list of securities that have had
          adjusted stock prices due to a corporate event after this date: YYYY'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of security name or ticker symbol with
          the returned results being the relevant securities in compacted list format
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Securities
  /securities/search:
    get:
      summary: Securities Search/Screener
      description: Returns a list of all securities that match the given conditions.
        The API call credits required for each call is equal to the number of conditions
        specified.
      operationId: securities-searchscreener
      x-api-path-slug: securitiessearch-get
      parameters:
      - in: query
        name: |-
          An operator


            Equal to: &ldquo;eq&rdquo;
        type: string
      - in: query
        name: conditions
        description: A comma
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
      - Market Data
      - Securities
  /historical_data:
    get:
      summary: Historical Data
      description: Returns the historical data for for a selected identifier (ticker
        symbol or index symbol) for a selected tag.  The complete list of tags available
        through this function are available here.  Income statement, cash flow statement,
        and ratios are returned as trailing twelve months values by default, but can
        be changed with the type parameter.  All other historical data points are
        returned as their value on a certain day based on filings reported as of that
        date.
      operationId: historical-data
      x-api-path-slug: historical-data-get
      parameters:
      - in: query
        name: end_date
        description: 'the latest date for which to return data: YYYY'
        type: string
      - in: query
        name: frequency
        description: 'the frequency of the historical prices &amp; valuation data:
          daily | weekly | monthly | quarterly | yearly'
        type: string
      - in: query
        name: identifier
        description: the stock market ticker symbol associated with the company&rsquo;s
          common stock or index
        type: string
      - in: query
        name: item
        description: the specified standardized tag requested
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: sequence
        description: in function)
        type: string
      - in: query
        name: show_date
        description: 'in, false by default) if true, the function will return the
          date value, and if false the function will return the data point value for
          a given query: true | false'
        type: string
      - in: query
        name: sort_order
        description: 'the order of the historical stock price dates: asc | desc'
        type: string
      - in: query
        name: start_date
        description: 'the earliest date for which to return data: YYYY'
        type: string
      - in: query
        name: type
        description: the type of periods requested
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical Data
  /prices/exchange:
    get:
      summary: Exchange Prices
      description: Returns professional-grade historical stock prices for all securities
        traded on a stock exchange for a single specified day.  Historical prices
        are available back to 1996 or the IPO date, with some companies with data
        back to the 1970s.
      operationId: exchange-prices
      x-api-path-slug: pricesexchange-get
      parameters:
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the stock market index:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: price_date
        description: the specified date in which historical stock prices are returned
          for a stock exchange
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Prices
      - Exchanges
  /companies/filings:
    get:
      summary: Company SEC Filings
      description: Returns the complete list of SEC filings for a company.
      operationId: company-sec-filings
      x-api-path-slug: companiesfilings-get
      parameters:
      - in: query
        name: end_date
        description: 'the last filing date for which to return filings, in the format:
          YYYY'
        type: string
      - in: query
        name: identifier
        description: the stock market ticker symbol associated with the company&rsquo;s
          common stock
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: report_type
        description: 'the report type of the filing requested: 10'
        type: string
      - in: query
        name: start_date
        description: 'the earliest filing date for which to return filings, in the
          format: YYYY'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Companies
      - Company Filings
  /fundamentals/standardized:
    get:
      summary: Standardized Fundamentals
      description: Returns a list of available standardized fundamentals (fiscal year
        and fiscal period) for a given ticker and statement.  Also, you may add a
        date and type parameter to specify the fundamentals you wish to be returned
        in the response.
      operationId: standardized-fundamentals
      x-api-path-slug: fundamentalsstandardized-get
      parameters:
      - in: query
        name: date
        description: 'the first fundamental will be the latest as of this specified
          date: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities:'
        type: string
      - in: query
        name: item
        description: in function)
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: sequence
        description: in function)
        type: string
      - in: query
        name: statement
        description: 'the financial statement requested, options include the income
          statement, balance sheet, statement of cash flows and calculated metrics
          and ratios: income_statement | balance_sheet | cash_flow_statement | calculations'
        type: string
      - in: query
        name: type
        description: the type of periods requested
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Fundamentals
  /financials/standardized:
    get:
      summary: Standardized Financials
      description: Returns professional-grade historical financial data.  This data
        is standardized, cleansed and verified to ensure the highest quality data
        sourced directly from the XBRL financial statements.  The primary purpose
        of standardized financials are to facilitate comparability across a single
        company&rsquo;s fundamentals and across all companies fundamentals.
      operationId: standardized-financials
      x-api-path-slug: financialsstandardized-get
      parameters:
      - in: query
        name: date
        description: 'the first fundamental will be the latest as of this specified
          date: YYYY'
        type: string
      - in: query
        name: fiscal_period
        description: 'the fiscal period associated with the fundamental: FY | Q1 |
          Q2 | Q3 | Q4 | Q1TTM | Q2TTM | Q3TTM | Q2YTD | Q3YTD'
        type: string
      - in: query
        name: fiscal_year
        description: 'the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: rounding
        description: 'ins function) ??? round the returned value (actuals, thousands,
          millions, billions): A | K | M | B'
        type: string
      - in: query
        name: sequence
        description: the sequence of the requested fundamental (i
        type: string
      - in: query
        name: statement
        description: 'the financial statement requested, options include the income
          statement, balance sheet, statement of cash flows and calculated metrics
          and ratios: income_statement | balance_sheet | cash_flow_statement | calculations'
        type: string
      - in: query
        name: tag
        description: in function)
        type: string
      - in: query
        name: type
        description: the type of periods requested
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Financials
  /tags/reported:
    get:
      summary: As Reported XBRL Tags and Labels
      description: Returns the As Reported XBRL tags and labels for a given ticker,
        statement, and date or fiscal year/fiscal quarter.
      operationId: as-reported-xbrl-tags-and-labels
      x-api-path-slug: tagsreported-get
      parameters:
      - in: query
        name: date
        description: 'the first fundamental will be the latest as of this specified
          date: YYYY'
        type: string
      - in: query
        name: fiscal_period
        description: 'the fiscal period associated with the fundamental: FY | Q1 |
          Q2 | Q3'
        type: string
      - in: query
        name: fiscal_year
        description: 'the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities:'
        type: string
      - in: query
        name: item
        description: in function)
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: sequence
        description: an integer 0 or greater for calling a single tag from the first
          entry, based on order
        type: string
      - in: query
        name: statement
        description: 'the financial statement requested: income_statement | balance_sheet
          | cash_flow_statement'
        type: string
      - in: query
        name: type
        description: the type of periods requested
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Tags
  /valuation/70087/assumptions:
    get:
      summary: Fetch Valuation Assumptions
      description: GET https://api.intrinio.com/valuation/:id/assumptions
      operationId: fetch-valuation-assumptions
      x-api-path-slug: valuation70087assumptions-get
      parameters:
      - in: query
        name: id
        description: the Intrinio unique identifier for the Valuation API request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Valuations
  /valuation/70087/outputs:
    get:
      summary: Fetch Valuation Outputs
      description: GET https://api.intrinio.com/valuation/:id/outputs
      operationId: fetch-valuation-outputs
      x-api-path-slug: valuation70087outputs-get
      parameters:
      - in: query
        name: id
        description: the Intrinio unique identifier for the Valuation API request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Valuations
  /companies/insider_transactions:
    get:
      summary: Insider Transactions by Company
      description: Returns a list of all insider transactions in a company.  Criteria
        for being an insider include being a director, officer, or 10%+ owner in the
        company.  Transactions are detailed for both non-derivative and derivative
        transactions by the insider.
      operationId: insider-transactions-by-company
      x-api-path-slug: companiesinsider-transactions-get
      parameters:
      - in: query
        name: end_date
        description: 'the latest transaction date for which to return data: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the Central Index Key issued by the SEC, which
          is the unique identifier all company filings are issued under:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: start_date
        description: 'the earliest transaction date for which to return data: YYYY'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Insider Transactions
  /owners/insider_transactions:
    get:
      summary: Insider Transactions By Owner
      description: Returns a list of all insider transactions by an owner in as many
        companies as the owner may be considered an insider.  Criteria for being an
        insider include being a director, officer, or 10%+ owner in the company.  Transactions
        are detailed for both non-derivative and derivative transactions by the insider.
      operationId: insider-transactions-by-owner
      x-api-path-slug: ownersinsider-transactions-get
      parameters:
      - in: query
        name: identifier
        description: the Central Index Key issued by the SEC, which is the unique
          identifier all owner filings are issued under:CENTRAL INDEX KEY
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Owners
      - Insider Transactions
  /owners:
    get:
      summary: Owners
      description: Returns owners list and information for all institutional owners
        of securities covered by Intrinio.  Includes detailed info for a single owner
        and the ability to query by name.
      operationId: owners
      x-api-path-slug: owners-get
      parameters:
      - in: query
        name: identifier
        description: the Central Index Key issued by the SEC, which is the unique
          identifier all owner filings are issued under:CENTRAL INDEX KEY
        type: string
      - in: query
        name: institutional
        description: (true)
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of owner name or cik id with the returned
          results being the relevant owners in compacted list format
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Owners
  /securities/institutional_ownership:
    get:
      summary: Institutional Owners by Security
      description: https://api.intrinio.com/securities/institutional_ownership?identifier={symbol}
      operationId: institutional-owners-by-security
      x-api-path-slug: securitiesinstitutional-ownership-get
      parameters:
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the Central Index Key issued by the SEC, which
          is the unique identifier all company filings are issued under:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Securities
      - Institutional Ownership
  /data_point:
    get:
      summary: Data Point
      description: Returns the most recent median data point for an Economic index
        for a selected tag.  The complete list of Economic Indices can be found here.  The
        complete list of Economic tags available through this function are available
        here.
      operationId: data-point
      x-api-path-slug: data-point-get
      parameters:
      - in: query
        name: identifier
        description: 'an identifier for the Economic Index selected:'
        type: string
      - in: query
        name: item
        description: 'the specified standardized tag or series ID requested: ECONOMIC
          TAGS'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Data
  /banks/holding_companies:
    get:
      summary: Bank Holding Companies
      description: Returns bank holding company list and information for all bank
        holding companies covered by Intrinio.
      operationId: bank-holding-companies
      x-api-path-slug: banksholding-companies-get
      parameters:
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: used to search for a ticker or bank name to return relevant banks
        type: string
      - in: query
        name: rssd_id
        description: 'the bank/bank holding company RSSD ID issued by the Federal
          Reserve: RSSD ID LOOKUP'
        type: string
      - in: query
        name: ticker
        description: 'the stock market ticker symbol associated with the companies
          common stock securities:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Holding Companies
      - Banks
  /banks/failed:
    get:
      summary: Failed Banks
      description: Returns failed bank list and information for all failed banks covered
        by Intrinio.
      operationId: failed-banks
      x-api-path-slug: banksfailed-get
      parameters:
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: used to search for a bank name to return relevant failed banks
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Failed Banks
  /tags/banks:
    get:
      summary: Bank XBRL Tags and Labels
      description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID,
        statement, and date or fiscal year/fiscal quarter.
      operationId: bank-xbrl-tags-and-labels
      x-api-path-slug: tagsbanks-get
      parameters:
      - in: query
        name: fiscal_period
        description: 'the fiscal period associated with the fundamental: FY | Q1 |
          Q2 | Q3 | Q4 | Q1TTM | Q2TTM | Q3TTM | Q2YTD | Q3YTD'
        type: string
      - in: query
        name: fiscal_year
        description: 'the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities, or the bank/bank holding company RSSD ID issued
          by the Federal Reserve:'
        type: string
      - in: query
        name: item
        description: in function)
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: sequence
        description: an integer 0 or greater for calling a single tag from the first
          entry
        type: string
      - in: query
        name: statement
        description: the financial statement requested from the call report, the UBPR
          report or Y
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Banks
  /stock_exchanges/corporate_actions:
    get:
      summary: Stock Exchange Corporate Actions
      description: 'Returns all corporate actions for all securities listed on a specified
        stock exchange.  A subscription to the EDI Corporate Actions Data Feed for
        a specific country will permit access to all stock exchanges in that country
        (ie, US includes NASDAQ, NYSE, BATS). Events 45+ types of corporate actions
        such as: Announcements and Annual Shareholder Meetings, Ex-date, Dividend
        pay date, Splits, Buy Backs, M&amp;A and Takeovers, Bankruptcies and much
        more'
      operationId: stock-exchange-corporate-actions
      x-api-path-slug: stock-exchangescorporate-actions-get
      parameters:
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the stock market index:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Stock Exchanges
  /options/expirations:
    get:
      summary: Option Expirations
      description: Returns all option contract expiration dates for a given ticker.
      operationId: option-expirations
      x-api-path-slug: optionsexpirations-get
      parameters:
      - in: query
        name: ticker
        description: the option ticker symbol, corresponding to the underlying security
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Options
  /options/historical:
    get:
      summary: Historical Prices
      description: Returns the historical prices for the given option contract.
      operationId: historical-prices
      x-api-path-slug: optionshistorical-get
      parameters:
      - in: query
        name: expiration
        description: the contract expiration date, in the format YYYY
        type: string
      - in: query
        name: identifier
        description: 'the contract identifier (example: AAPL190118C00195000)'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: strike
        description: the contract strike price
        type: string
      - in: query
        name: ticker
        description: the option ticker symbol, corresponding to the underlying security
        type: string
      - in: query
        name: type
        description: the contract type, either put or call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Options
      - Historical
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
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