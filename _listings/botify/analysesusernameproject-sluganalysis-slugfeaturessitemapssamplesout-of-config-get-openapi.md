---
swagger: "2.0"
x-collection-name: Botify
x-complete: 0
info:
  title: Botify Get Analyses Username Project Slug Analysis Slug Features Sitemaps
    Samples Out Of Config
  description: Sample list of URLs which were found in your sitemaps but outside of
    the crawl perimeter defined for the project, for instance domain/subdomain or
    protocol (HTTP/HTTPS) not allowed in the crawl settings.
  version: 1.0.0
host: api.botify.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /analyses/{username}/{project_slug}/{analysis_slug}/features/sitemaps/samples/out_of_config:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Sitemaps
        Samples Out Of Config
      description: Sample list of URLs which were found in your sitemaps but outside
        of the crawl perimeter defined for the project, for instance domain/subdomain
        or protocol (HTTP/HTTPS) not allowed in the crawl settings.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesOutOfConfig
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapssamplesout-of-config-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Samples
      - Out
      - Of
      - Config
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