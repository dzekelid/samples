{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug Features Sitemaps Samples Out Of Config",
    "_postman_id": "bc2520d6-b30c-4702-8008-7f91053cfaaf",
    "description": "Sample list of URLs which were found in your sitemaps but outside of the crawl perimeter defined for the project, for instance domain/subdomain or protocol (HTTP/HTTPS) not allowed in the crawl settings.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "23000f7f-b0ca-4c41-8179-d4d0fa81be4e",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesOutOfConfig",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug/features/sitemaps/samples/out_of_config"
              ],
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "size",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "project_slug",
                  "value": "project_slug",
                  "type": "string"
                },
                {
                  "id": "analysis_slug",
                  "value": "analysis_slug",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Sample list of URLs which were found in your sitemaps but outside of the crawl perimeter defined for the project, for instance domain/subdomain or protocol (HTTP/HTTPS) not allowed in the crawl settings."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e74b2912-ddef-4f8b-8dfc-943a9ddfcbe0"
            }
          ]
        }
      ]
    }
  ]
}