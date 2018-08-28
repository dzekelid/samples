---
name: Fire Browse
x-slug: fire-browse
description: A simple and elegant way to explore cancer data. Sitting above one of
  the deepest and most integratively characterized open cancer datasets in the world.
  Backed by a powerful computational infrastructure, application programming interface
  (API), graphical tools and online reports. With over 80K sample aliquots from 11,000+
  cancer patients, spanning 38 unique disease cohorts.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Samples
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/apis.md
specificationVersion: "0.14"
apis:
- name: Fire Browse Beta API - Retrieve TCGA CDEs verbatim, i.e. not normalized by
    Firehose.
  x-api-slug: samplesclinical-get
  description: This service returns patient clinical data from TCGA, verbatim. It
    differs from the Samples/Clinical_FH method by providing access to all TCGA CDEs
    in their original form, not merely the subset of CDEs normalized by Firehose for
    analyses.  Results may be selected by disease cohort, patient barcode or CDE name,
    but at least one cohort, barcode, or CDE must be provided. When filtering by CDE
    note that only when a patient record contains one or more of the selected CDEs
    will it be returned. Visit the Metadata/ClinicalNames api function to see the
    entire list of TCGA CDEs that may be queried via this method. For more information
    on how clinical data are processed, see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Cancer, API Provider, Data Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesclinical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesclinical-get-openapi.md
- name: Fire Browse Beta API - Retrieve CDEs normalized by Firehose and selected for
    analyses.
  x-api-slug: samplesclinical-fh-get
  description: This service returns patient-level clinical data elements (CDEs) that
    have been normalized by Firehose for use in analyses. Results may be selected
    by disease cohort, patient barcode or CDE name, but at least one cohort, barcode
    or CDE must be provided. When filtering by CDE note that only when a  patient
    record contains one or more of the selected CDEs will it be returned. Visit this
    table of CDEs to see what's available for every disase cohort; for more information
    on how these CDEs are processed see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Cancer, API Provider, Data Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesclinical-fh-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesclinical-fh-get-openapi.md
- name: Fire Browse Beta API - Retrieve mRNASeq data.
  x-api-slug: samplesmrnaseq-get
  description: This service returns sample-level log2 mRNASeq expression values. Results
    may be filtered by gene, cohort, barcode, sample type or characterization protocol,
    but at least one gene must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Cancer, API Provider, Data Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesmrnaseq-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesmrnaseq-get-openapi.md
- name: Fire Browse Beta API - Retrieve miRSeq data.
  x-api-slug: samplesmirseq-get
  description: This service returns sample-level log2 miRSeq expression values. Results
    may be filtered by miR, cohort, barcode, sample type or Firehose preprocessing
    tool, but at least one miR must be supplied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Cancer, API Provider, Data Provider, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesmirseq-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/samples/master/_listings/fire-browse/samplesmirseq-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://factual.api.gallery.streamdata.io
- type: x-api-stack
  url: http://fire.browse.stack.network
- type: x-website
  url: http://firebrowse.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---