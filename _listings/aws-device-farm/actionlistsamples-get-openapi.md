---
swagger: "2.0"
x-collection-name: AWS Device Farm
x-complete: 0
info:
  title: AWS Device Farm API List Samples
  version: 1.0.0
  description: Gets information about samples, given an AWS Device Farm project ARN.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListSamples:
    get:
      summary: List Samples
      description: Gets information about samples, given an AWS Device Farm project
        ARN.
      operationId: listSamples
      x-api-path-slug: actionlistsamples-get
      parameters:
      - in: query
        name: arn
        description: The Amazon Resource Name (ARN) of the project for which you want
          to list samples
        type: string
      - in: query
        name: nextToken
        description: An identifier that was returned from the previous call to this
          operation, which can be used to return the next set of items in the list
        type: string
      responses:
        200:
          description: OK
      tags:
      - Samples
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