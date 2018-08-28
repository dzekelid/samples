swagger: "2.0"
x-collection-name: AWS Device Farm
x-complete: 1
info:
  title: AWS Device Farm API
  version: 1.0.0
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