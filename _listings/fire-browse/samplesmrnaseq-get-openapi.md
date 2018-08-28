---
swagger: "2.0"
x-collection-name: Fire Browse
x-complete: 0
info:
  title: Fire Browse Beta API Retrieve mRNASeq data.
  description: This service returns sample-level log2 mRNASeq expression values. Results
    may be filtered by gene, cohort, barcode, sample type or characterization protocol,
    but at least one gene must be supplied.
  version: 1.1.35 (2016-09-27 10:12:23 6a47e74011281b2aa
host: firebrowse.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Samples/Clinical:
    get:
      summary: Retrieve TCGA CDEs verbatim, i.e. not normalized by Firehose.
      description: This service returns patient clinical data from TCGA, verbatim.
        It differs from the Samples/Clinical_FH method by providing access to all
        TCGA CDEs in their original form, not merely the subset of CDEs normalized
        by Firehose for analyses.  Results may be selected by disease cohort, patient
        barcode or CDE name, but at least one cohort, barcode, or CDE must be provided.
        When filtering by CDE note that only when a patient record contains one or
        more of the selected CDEs will it be returned. Visit the Metadata/ClinicalNames
        api function to see the entire list of TCGA CDEs that may be queried via this
        method. For more information on how clinical data are processed, see our pipeline
        documentation.
      operationId: getSamplesClinical
      x-api-path-slug: samplesclinical-get
      parameters:
      - in: query
        name: cde_name
        description: Retrieve results only for specified CDEs, per the Metadata/ClinicalNames
          function
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Samples
      - Clinical
  /Samples/Clinical_FH:
    get:
      summary: Retrieve CDEs normalized by Firehose and selected for analyses.
      description: This service returns patient-level clinical data elements (CDEs)
        that have been normalized by Firehose for use in analyses. Results may be
        selected by disease cohort, patient barcode or CDE name, but at least one
        cohort, barcode or CDE must be provided. When filtering by CDE note that only
        when a  patient record contains one or more of the selected CDEs will it be
        returned. Visit this table of CDEs to see what's available for every disase
        cohort; for more information on how these CDEs are processed see our pipeline
        documentation.
      operationId: getSamplesClinicalFh
      x-api-path-slug: samplesclinical-fh-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: fh_cde_name
        description: Retrieve results only for the CDEs specified from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Samples
      - Clinical
      - FH
  /Samples/mRNASeq:
    get:
      summary: Retrieve mRNASeq data.
      description: This service returns sample-level log2 mRNASeq expression values.
        Results may be filtered by gene, cohort, barcode, sample type or characterization
        protocol, but at least one gene must be supplied.
      operationId: getSamplesMrnaseq
      x-api-path-slug: samplesmrnaseq-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: gene
        description: Comma separated list of gene name(s)
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: protocol
        description: Narrow search to one or more sample characterization protocols
          from the scrollable list
      - in: query
        name: sample_type
        description: Narrow search to one or more TCGA sample types from the scrollable
          list
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      - in: query
        name: tcga_participant_barcode
        description: Comma separated list of TCGA participant barcodes (e
      responses:
        200:
          description: OK
      tags:
      - Samples
      - MRNASeq
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