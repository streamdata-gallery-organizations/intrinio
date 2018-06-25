---
name: Intrinio
x-slug: intrinio
description: Intelligent Data, On Demand. The financial data platform for developers,
  investors, students, and educators, with over 200 feeds including real-time, intraday,
  EOD, and international financial data available via REST API, WebSocket, CSV, Excel,
  and Goo...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
x-kinRank: "8"
x-alexaRank: "303229"
tags: Intrinio
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/apis.md
specificationVersion: "0.14"
apis:
- name: Intrinio API Company Master
  x-api-slug: intrinio-api
  description: Returns the master list of all companies covered by the Intrinio Data
    Marketplace.  You can view the Company/Security Master here.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////companies
  tags: Market Data,Companies
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/companies-get-openapi.md
- name: Intrinio API Index Master
  x-api-slug: intrinio-api
  description: 'Returns indices list and information for all indices covered by Intrinio.
    There are three distinct types of indices: Stock Market, SIC (Sector &amp; Industry),
    and Economic.  You can view the Stock Market Indices Master, SIC Indices Master,
    and the Economic Indices Master.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////indices
  tags: Market Data,Indices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/indices-get-openapi.md
- name: Intrinio API Stock Exchange Master
  x-api-slug: intrinio-api
  description: Returns stock exchange list and information for all stock exchanges
    covered by Intrinio.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////stock_exchanges
  tags: Market Data,Stock Exchanges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/stock-exchanges-get-openapi.md
- name: Intrinio API Securities
  x-api-slug: intrinio-api
  description: Returns security list and information for all securities covered by
    Intrinio.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////securities
  tags: Market Data,Securities
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/securities-get-openapi.md
- name: Intrinio API Securities Search/Screener
  x-api-slug: intrinio-api
  description: Returns a list of all securities that match the given conditions. The
    API call credits required for each call is equal to the number of conditions specified.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////securities/search
  tags: Market Data,Securities
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/securitiessearch-get-openapi.md
- name: Intrinio API Historical Data
  x-api-slug: intrinio-api
  description: Returns the historical data for for a selected identifier (ticker symbol
    or index symbol) for a selected tag.  The complete list of tags available through
    this function are available here.  Income statement, cash flow statement, and
    ratios are returned as trailing twelve months values by default, but can be changed
    with the type parameter.  All other historical data points are returned as their
    value on a certain day based on filings reported as of that date.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////historical_data
  tags: Market Data,Historical Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/historical-data-get-openapi.md
- name: Intrinio API Exchange Prices
  x-api-slug: intrinio-api
  description: Returns professional-grade historical stock prices for all securities
    traded on a stock exchange for a single specified day.  Historical prices are
    available back to 1996 or the IPO date, with some companies with data back to
    the 1970s.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////prices/exchange
  tags: Market Data,Prices,Exchanges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/pricesexchange-get-openapi.md
- name: Intrinio API Company SEC Filings
  x-api-slug: intrinio-api
  description: Returns the complete list of SEC filings for a company.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////companies/filings
  tags: Market Data,Companies,Company Filings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/companiesfilings-get-openapi.md
- name: Intrinio API Standardized Fundamentals
  x-api-slug: intrinio-api
  description: Returns a list of available standardized fundamentals (fiscal year
    and fiscal period) for a given ticker and statement.  Also, you may add a date
    and type parameter to specify the fundamentals you wish to be returned in the
    response.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////fundamentals/standardized
  tags: Market Data,Fundamentals
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/fundamentalsstandardized-get-openapi.md
- name: Intrinio API Standardized Financials
  x-api-slug: intrinio-api
  description: Returns professional-grade historical financial data.  This data is
    standardized, cleansed and verified to ensure the highest quality data sourced
    directly from the XBRL financial statements.  The primary purpose of standardized
    financials are to facilitate comparability across a single company&rsquo;s fundamentals
    and across all companies fundamentals.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////financials/standardized
  tags: Market Data,Financials
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/financialsstandardized-get-openapi.md
- name: Intrinio API As Reported XBRL Tags and Labels
  x-api-slug: intrinio-api
  description: Returns the As Reported XBRL tags and labels for a given ticker, statement,
    and date or fiscal year/fiscal quarter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////tags/reported
  tags: Market Data,Tags
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/tagsreported-get-openapi.md
- name: Intrinio API Fetch Valuation Assumptions
  x-api-slug: intrinio-api
  description: GET https://api.intrinio.com/valuation/:id/assumptions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////valuation/70087/assumptions
  tags: Market Data,Valuations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/valuation70087assumptions-get-openapi.md
- name: Intrinio API Fetch Valuation Outputs
  x-api-slug: intrinio-api
  description: GET https://api.intrinio.com/valuation/:id/outputs
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////valuation/70087/outputs
  tags: Market Data,Valuations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/valuation70087outputs-get-openapi.md
- name: Intrinio API Insider Transactions by Company
  x-api-slug: intrinio-api
  description: Returns a list of all insider transactions in a company.  Criteria
    for being an insider include being a director, officer, or 10%+ owner in the company.  Transactions
    are detailed for both non-derivative and derivative transactions by the insider.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////companies/insider_transactions
  tags: Market Data,Insider Transactions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/companiesinsider-transactions-get-openapi.md
- name: Intrinio API Insider Transactions By Owner
  x-api-slug: intrinio-api
  description: Returns a list of all insider transactions by an owner in as many companies
    as the owner may be considered an insider.  Criteria for being an insider include
    being a director, officer, or 10%+ owner in the company.  Transactions are detailed
    for both non-derivative and derivative transactions by the insider.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////owners/insider_transactions
  tags: Market Data,Owners,Insider Transactions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/ownersinsider-transactions-get-openapi.md
- name: Intrinio API Owners
  x-api-slug: intrinio-api
  description: Returns owners list and information for all institutional owners of
    securities covered by Intrinio.  Includes detailed info for a single owner and
    the ability to query by name.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////owners
  tags: Market Data,Owners
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/owners-get-openapi.md
- name: Intrinio API Institutional Owners by Security
  x-api-slug: intrinio-api
  description: https://api.intrinio.com/securities/institutional_ownership?identifier={symbol}
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////securities/institutional_ownership
  tags: Market Data,Securities,Institutional Ownership
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/securitiesinstitutional-ownership-get-openapi.md
- name: Intrinio API Data Point
  x-api-slug: intrinio-api
  description: Returns the most recent median data point for an Economic index for
    a selected tag.  The complete list of Economic Indices can be found here.  The
    complete list of Economic tags available through this function are available here.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////data_point
  tags: Market Data,Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/data-point-get-openapi.md
- name: Intrinio API Bank Holding Companies
  x-api-slug: intrinio-api
  description: Returns bank holding company list and information for all bank holding
    companies covered by Intrinio.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////banks/holding_companies
  tags: Market Data,Holding Companies,Banks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/banksholding-companies-get-openapi.md
- name: Intrinio API Failed Banks
  x-api-slug: intrinio-api
  description: Returns failed bank list and information for all failed banks covered
    by Intrinio.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////banks/failed
  tags: Market Data,Failed Banks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/banksfailed-get-openapi.md
- name: Intrinio API Bank XBRL Tags and Labels
  x-api-slug: intrinio-api
  description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID, statement,
    and date or fiscal year/fiscal quarter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////tags/banks
  tags: Market Data,Banks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/tagsbanks-get-openapi.md
- name: Intrinio API Stock Exchange Corporate Actions
  x-api-slug: intrinio-api
  description: 'Returns all corporate actions for all securities listed on a specified
    stock exchange.  A subscription to the EDI Corporate Actions Data Feed for a specific
    country will permit access to all stock exchanges in that country (ie, US includes
    NASDAQ, NYSE, BATS). Events 45+ types of corporate actions such as: Announcements
    and Annual Shareholder Meetings, Ex-date, Dividend pay date, Splits, Buy Backs,
    M&amp;A and Takeovers, Bankruptcies and much more'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////stock_exchanges/corporate_actions
  tags: Market Data,Stock Exchanges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/stock-exchangescorporate-actions-get-openapi.md
- name: Intrinio API Option Expirations
  x-api-slug: intrinio-api
  description: Returns all option contract expiration dates for a given ticker.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////options/expirations
  tags: Market Data,Options
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/optionsexpirations-get-openapi.md
- name: Intrinio API Historical Prices
  x-api-slug: intrinio-api
  description: Returns the historical prices for the given option contract.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////options/historical
  tags: Market Data,Options,Historical
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/optionshistorical-get-openapi.md
- name: Intrinio API Sector News Sentiments
  x-api-slug: intrinio-api
  description: Returns daily summaries of news sentiments by sector and date.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////news_sector_sentiments
  tags: Market Data,News,Sector, Sentiments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/news-sector-sentiments-get-openapi.md
- name: Intrinio API Bloggers
  x-api-slug: intrinio-api
  description: Returns a list of bloggers. TipRanks bloggers are anonymized, but you
    will be able to reference them with the provided id field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////bloggers
  tags: Market Data,Bloggers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/bloggers-get-openapi.md
- name: Intrinio API Blogger Ratings
  x-api-slug: intrinio-api
  description: Returns blogger buy/sell/hold ratings for a specific security and date.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////blogger_ratings
  tags: Market Data,Blogger Ratings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/blogger-ratings-get-openapi.md
- name: Intrinio API Analysts
  x-api-slug: intrinio-api
  description: Returns a list of analysts. TipRanks analysts are anonymized, but you
    will be able to reference them with the provided id field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////analysts
  tags: Market Data,Analysts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/analysts-get-openapi.md
- name: Intrinio API Analyst Ratings
  x-api-slug: intrinio-api
  description: Returns analyst buy/sell/hold ratings for a specific security and date,
    as well as target prices.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////analyst_ratings
  tags: Market Data,Analyst Ratings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/analyst-ratings-get-openapi.md
- name: Intrinio API Press Releases
  x-api-slug: intrinio-api
  description: Returns the most recent press releases by Nasdaq GlobeNewsire for a
    company.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////press_releases
  tags: Market Data,Press Releases
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/press-releases-get-openapi.md
- name: Intrinio API Executive Master
  x-api-slug: intrinio-api
  description: Returns a list of all executives and their unique executive identifier,
    including both U.S. and International executives.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////executives
  tags: Market Data,Executives
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/executives-get-openapi.md
- name: Intrinio API Company Executive Contacts
  x-api-slug: intrinio-api
  description: Returns a list of all information for an executive and their related
    companies.  Information includes the unique Intrinio executive company identifier,
    and detailed contact information for the executive at a specified company.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////executives/companies
  tags: Market Data,Executives,companies
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/executivescompanies-get-openapi.md
- name: Intrinio API Company Executive Roles
  x-api-slug: intrinio-api
  description: For a specific executive company identifier, returns a list of all
    roles within the company.  For example, an executive may be the Chief Executive
    Officer, a Director, and the Chairman of the Board of Directors.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com////executives/roles
  tags: Market Data,Executives,Executive Roles
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/executivesroles-get-openapi.md
- name: Intrinio API
  x-api-slug: intrinio-api
  description: Intelligent Data, On Demand. The financial data platform for developers,
    investors, students, and educators, with over 200 feeds including real-time, intraday,
    EOD, and international financial data available via REST API, WebSocket, CSV,
    Excel, and Goo...
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28077-intrinio.jpg
  humanURL: https://intrinio.com
  baseURL: https://api.intrinio.com//
  tags: Intrinio
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/intrinio/master/_listings/intrinio/openapi.md
x-common:
- type: x-applications-showcase
  url: https://intrinio.com/marketplace/apps
- type: x-authentication
  url: http://docs.intrinio.com/#authentication
- type: x-blog
  url: http://blog.intrinio.com/
- type: x-blog-rss
  url: http://blog.intrinio.com/feed/
- type: x-code
  url: http://docs.intrinio.com/#sdks
- type: x-crunchbase
  url: https://crunchbase.com/organization/tribunat
- type: x-developer
  url: https://intrinio.com/we-love-developers
- type: x-documentation
  url: https://intrinio.com/marketplace/data
- type: x-email
  url: cfarley@intrinio.com
- type: x-email
  url: admin@intrinio.com
- type: x-email
  url: support@intrinio.com
- type: x-email
  url: acarpenter@intrinio.com
- type: x-login
  url: https://intrinio.com/login
- type: x-partners
  url: https://intrinio.com/partners
- type: x-press
  url: https://intrinio.com/press
- type: x-rate-limits
  url: http://docs.intrinio.com/#limits
- type: x-selfservice-registration
  url: https://intrinio.com/signup
- type: x-spreadsheets
  url: http://docs.intrinio.com/#spreadsheet-add-ins
- type: x-support
  url: https://intrinio.com/help
- type: x-tutorial
  url: https://intrinio.com/tutorial/web_api
- type: x-twitter
  url: https://twitter.com/intrinio
- type: x-website
  url: https://intrinio.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---