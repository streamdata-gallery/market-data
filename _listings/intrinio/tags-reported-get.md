---
swagger: "2.0"
info:
  title: Intrinio API As Reported XBRL Tags and Labels
  description: Returns the As Reported XBRL tags and labels for a given ticker, statement,
    and date or fiscal year/fiscal quarter.
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
  /tags/reported:
    get:
      summary: As Reported XBRL Tags and Labels
      description: Returns the As Reported XBRL tags and labels for a given ticker,
        statement, and date or fiscal year/fiscal quarter
      operationId: as-reported-xbrl-tags-and-labels
      parameters:
      - in: query
        name: date
        description: ' the first fundamental will be the latest as of this specified
          date: YYYY'
        type: string
      - in: query
        name: fiscal_period
        description: ' the fiscal period associated with the fundamental: FY | Q1
          | Q2 | Q3'
        type: string
      - in: query
        name: fiscal_year
        description: ' the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: ' the stock market ticker symbol associated with the companies
          common stock securities: '
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
          entry, based on order'
        type: string
      - in: query
        name: statement
        description: ' the financial statement requested: income_statement | balance_sheet
          | cash_flow_statement'
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
      - tags
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