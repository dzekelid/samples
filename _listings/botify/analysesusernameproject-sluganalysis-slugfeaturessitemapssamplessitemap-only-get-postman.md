{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug Features Sitemaps Samples Sitemap Only",
    "_postman_id": "dbea56e2-88de-4212-8255-fcce8160cfe3",
    "description": "Sample list of URLs which were found in your sitemaps, within the project allowed scope (allowed domains/subdomains/protocols), but not found by the Botify crawler.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "2af3458d-5de1-45a3-9f8e-f8b5a21316c5",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesSitemapOnly",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug/features/sitemaps/samples/sitemap_only"
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
            "description": "Sample list of URLs which were found in your sitemaps, within the project allowed scope (allowed domains/subdomains/protocols), but not found by the Botify crawler."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f4314943-3fd9-42e1-b962-cc598c87b91f"
            }
          ]
        }
      ]
    }
  ]
}