{
  "info": {
    "name": "Fire Browse Beta API Retrieve TCGA CDEs verbatim, i.e. not normalized by Firehose.",
    "_postman_id": "1787e722-5b92-439d-8bfa-42584493e5e0",
    "description": "This service returns patient clinical data from TCGA, verbatim. It differs from the Samples/Clinical_FH method by providing access to all TCGA CDEs in their original form, not merely the subset of CDEs normalized by Firehose for analyses.  Results may be selected by disease cohort, patient barcode or CDE name, but at least one cohort, barcode, or CDE must be provided. When filtering by CDE note that only when a patient record contains one or more of the selected CDEs will it be returned. Visit the Metadata/ClinicalNames api function to see the entire list of TCGA CDEs that may be queried via this method. For more information on how clinical data are processed, see our pipeline documentation.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "72ff7fad-714b-4213-a154-1b4b3270fef0",
          "name": "getAnalysesCopynumberGenesAll",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/All?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 all_data_by_genes.txt output data. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59adc1e1-02b6-4ec3-a0e9-a1f9a157ec8f"
            }
          ]
        },
        {
          "id": "0ab0ca15-ad4d-4726-9dc7-d9dda323a724",
          "name": "getAnalysesCopynumberGenesAmplified",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Amplified?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 amp_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9e770ebd-256f-4846-9db4-3a6e8b53daa1"
            }
          ]
        },
        {
          "id": "8523d573-c812-47b3-ad30-c6f78daf02e8",
          "name": "getAnalysesCopynumberGenesDeleted",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Deleted?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 del_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e54df411-a6a7-4cf3-9b52-b46279400498"
            }
          ]
        },
        {
          "id": "f615bc03-5b98-467e-9704-4b8e99d21892",
          "name": "getAnalysesCopynumberGenesFocal",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Focal?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 focal_data_by_genes.txt output data. This output is similar to the all_data_by_genes.txt output, but using only focal events with lengths greater than the  focal length cutoff. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, and/or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5d769c7-737c-42e0-ac6a-18137880093b"
            }
          ]
        },
        {
          "id": "606a0aef-5f1f-4c77-b1b2-cf2ab333ccc0",
          "name": "getAnalysesCopynumberGenesThresholded",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/CopyNumber/Genes/Thresholded?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides access to the Gistic2 all_thresholded_by_genes.txt output data. A gene-level table of discrete amplification and deletion indicators for all samples. A table value of 0 means no amplification or deletion above the threshold. Amplifications are positive numbers: 1 means amplification above the amplification threshold; 2 means amplifications larger to the arm level amplifications observed for the sample. Deletions are represented by negative table values: -1 represents deletion beyond the threshold; -2 means deletions greater than the minimum arm-level deletion observed for the sample. Results maybe filtered by cohort, gene or barcode, but at least one gene or barcode must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "41d041ff-3dc6-425a-96c3-11cb2ef21df2"
            }
          ]
        },
        {
          "id": "77caf8ae-6574-43a7-a1b5-1000c85446ff",
          "name": "getAnalysesFeaturetable",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/FeatureTable?cohort=%7B%7D&column=%7B%7D&date=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns part or all of the so-called feature table; which aggregates the most important findings across ALL pipelines in the GDAC Firehose analysis workflow into a single table for simple access.  One feature table is created per disease cohort.  Results may be filtered by date or cohort, but at least 1 cohort must be specified here. For more details please visit the online documentation.  Please note that the service is still undergoing experimental evaluation and does not return JSON format."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e03439cf-d3b8-4ca7-aa73-065be9b2f941"
            }
          ]
        },
        {
          "id": "32c7515a-c1b8-4c1d-abcc-ac918b517c7f",
          "name": "getAnalysesMutationMaf",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Mutation/MAF?cohort=%7B%7D&column=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns columns from the MAF generated by MutSig. Results may be filtered by gene, cohort, tool, or barcode, but at least one gene OR barcode OR cohort must be given.  By default a subset consisting of the most commonly used columns will be returned, but that can be modified with the column parameter. Specifying 'all' in this parameter is a convenient way to return every column of the respective MAF, and has precedence over any any other column selection expression.  The complete list of column names that may be specified is given here.  For more information on the mutation data, and how it is processed by Firehose, please consult the pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1c4068ed-b8e3-48c7-8df9-7f8827187d68"
            }
          ]
        },
        {
          "id": "39ed0f54-360d-4a6a-9bef-da0f7f966b5c",
          "name": "getAnalysesMutationSmg",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Mutation/SMG?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&q=%7B%7D&rank=%7B%7D&sort_by=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service provides a list of significantly mutated genes, as scored by MutSig.  It may be filtered by cohort, rank, gene, tool and/or Q-value threshold, but at least one cohort or gene must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "750b9b82-3e92-4424-81a6-da91e49cda5c"
            }
          ]
        },
        {
          "id": "8ee44684-23d6-419a-809b-009094febc54",
          "name": "getAnalysesReports",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/Reports?cohort=%7B%7D&date=%7B%7D&format=%7B%7D&name=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns URLs to the analysis result reports for runs of the Broad Institute GDAC Firehose analysis pipeline. At least one year of run reports are maintained in the database, but the reports from the latest run will be returned by default. The set of Nozzle reports returned may be filtered by disease cohort, report type and report name."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f43aafa3-f840-43b5-9e7e-5e8c7e09b686"
            }
          ]
        },
        {
          "id": "2c91c40f-eddd-4fc2-bc97-e13bdaf0358d",
          "name": "getAnalysesMrnaseqQuartiles",
          "request": {
            "url": "http://firebrowse.org/api/v1/Analyses/mRNASeq/Quartiles?cohort=%7B%7D&Exclude=%7B%7D&format=%7B%7D&gene=%7B%7D&protocol=%7B%7D&sample_type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "For a given gene compute quartiles and extrema, suitable e.g. for drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample type, patient barcode  or characterization protocol, and are returned sorted by cohort.  Note that samples for which no expression value was recorded (e.g. the melanoma sample TCGA-GN-262) are removed prior to calculation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4cbc8ec9-e8e1-48e6-b7f8-81105aab7b54"
            }
          ]
        }
      ]
    },
    {
      "name": "Archives",
      "item": [
        {
          "id": "569699c6-969b-4118-aee6-55c019a30828",
          "name": "getArchivesStandarddata",
          "request": {
            "url": "http://firebrowse.org/api/v1/Archives/StandardData?center=%7B%7D&cohort=%7B%7D&data_type=%7B%7D&date=%7B%7D&format=%7B%7D&level=%7B%7D&page=%7B%7D&page_size=%7B%7D&platform=%7B%7D&protocol=%7B%7D&sort_by=%7B%7D&tool=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns the archive URLs for our Firehose standard data runs, providing a RESTful interface similar in spirit to the command line firehose_get tool. The archives can be filtered based on date, cohort, data type, platform, center, data level, and protocol."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fb2518c8-0f28-4c44-aeb4-3aec18319d35"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "357d9bde-5579-49e0-b3c9-7246bbe2bbb4",
          "name": "getMetadataCenters",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Centers?center=%7B%7D&format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all consortium members in TCGA, aka centers; it provides both the HTTP domain and full organizational name of each center.  A subset of this table may be obtained by explicitly specifying one or more domain names."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11b65224-3a21-43f0-bbbd-e95fca100830"
            }
          ]
        },
        {
          "id": "820944c8-240e-4038-b584-f7bfb4e6d066",
          "name": "getMetadataClinicalnames",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/ClinicalNames?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve names of all patient-level clinical data elements (CDES) available in TCGA, unioned across all disease cohorts. A CDE will be listed here only when it has a value other than NA for at least 1 patient case in any disease cohort. For more information on how these CDEs are processed see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a58005c7-d6ea-424a-b52d-c3a0261fd0c1"
            }
          ]
        },
        {
          "id": "79cff41a-2419-474c-b394-e7e53aa96d1e",
          "name": "getMetadataClinicalnamesFh",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/ClinicalNames_FH?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns the names of patient-level clinical data elements (CDEs) that have been normalized by Firehose for use in analyses, unioned across all disease cohorts. For more information on how these CDEs are processed, see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e436073-4c1f-4037-b70d-d52bf77a4722"
            }
          ]
        },
        {
          "id": "2af69bc5-96c8-4458-aabf-d865bf6879db",
          "name": "getMetadataCohorts",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Cohorts?cohort=%7B%7D&format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table containing all TCGA cohort abbreviations and their corresponding disease names.  A subset of that table may be obtained by explicitly specifying one or more cohort abbreviations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4a2c408-bb75-458c-9682-2e9ed5bc1108"
            }
          ]
        },
        {
          "id": "30832837-4c00-424d-9b02-4f490453e182",
          "name": "getMetadataCounts",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Counts?cohort=%7B%7D&data_type=%7B%7D&date=%7B%7D&format=%7B%7D&sample_type=%7B%7D&sort_by=%7B%7D&totals=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the aliquot counts for each disease cohort, per sample\ntype and data type.  The sample type designation of \"Tumor\"\nmay be used to aggregate the count of all tumor aliquots into\na single number per disease and data type. See the SampleTypes\nfunction for a complete description of sample types."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ab1be8d8-b693-48cc-a213-0119e1446e4e"
            }
          ]
        },
        {
          "id": "492c01ea-57b2-409b-bf4d-9912b67d929d",
          "name": "getMetadataDates",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Dates?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve datestamps of all gdac firehose standard data and analyses runs that have been ingested into firebrowse.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc251440-365e-4ab2-ae60-001f351439e1"
            }
          ]
        },
        {
          "id": "ebed954a-badf-4756-9dfd-12ad286a2d40",
          "name": "getMetadataHeartbeat",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/HeartBeat?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a message to indicate that API (server) is up and running, or times out if not."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eaecae1d-3565-4941-b386-f7aeb9e656be"
            }
          ]
        },
        {
          "id": "6c6ebc6f-fc87-4707-9d0d-0fd56309c11a",
          "name": "getMetadataMafcolnames",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/MAFColNames?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the names of all columns in the mutation annotation files (MAFs) hosted by FireBrowse.  For more information on the mutation data, and how it is processed by Firehose, please consult the pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fdad5588-8d3f-47e8-af9c-fa7ff0dc2ebe"
            }
          ]
        },
        {
          "id": "910b31b5-2ada-4dc9-92ac-c203d53166e5",
          "name": "getMetadataPatients",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Patients?cohort=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns a list of all TCGA patient barcodes in FireBrowse, optionally filtered by disease cohort.  The barcodes are obtained directy from the clinical data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4d043a70-d63a-4128-8a46-1c1d9beb11c9"
            }
          ]
        },
        {
          "id": "747716b6-f233-405f-836e-963dd55410bc",
          "name": "getMetadataPlatforms",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/Platforms?format=%7B%7D&platform=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all of the technology platforms used to sequence or characterize samples in TCGA--both their short platform codes and full names.  A subset of this table may be obtained by explicitly specifying one or more platform codes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6d44a0f4-3c63-4824-82f6-0cb67f634153"
            }
          ]
        },
        {
          "id": "b007b20d-bc34-4026-97d0-4314275cc4be",
          "name": "getMetadataSampletypeBarcodeTcgaBarcode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/Barcode/:TCGA_Barcode"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "TCGA_Barcode",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Given a tcga barcode, return its short letter sample type code.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86c6f248-7463-4000-b320-0434a748384c"
            }
          ]
        },
        {
          "id": "cfa2b4bd-3083-493b-982a-1e4d15ed74cb",
          "name": "getMetadataSampletypeCodeCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/Code/:code"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Convert a TCGA numeric sample type code (e.g. 01, 02) to its corresponding symbolic (short letter) code (e.g. TP, TR)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbe9faab-add7-44f2-a446-23a3ed052415"
            }
          ]
        },
        {
          "id": "e7cd48e0-0712-4511-8d57-d957ed40ca71",
          "name": "getMetadataSampletypeShortlettercodeShortLetterCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "firebrowse.org",
              "path": [
                "api",
                "v1",
                "Metadata/SampleType/ShortLetterCode/:short_letter_code"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "short_letter_code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Convert a TCGA sample type code in symbolic form (or 'short letter code' like TP, TR) to its corresponding numeric form (e.g. 01, 02)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8434a574-3ca3-406e-874e-752346a9d1d2"
            }
          ]
        },
        {
          "id": "24e970fa-0970-4abe-a4c2-f988eba3d266",
          "name": "getMetadataSampletypes",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/SampleTypes?format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return all tcga sample type codes, both numeric and symbolic.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f786f4fb-91e7-4508-8d1f-99b88e51823b"
            }
          ]
        },
        {
          "id": "02bb10e8-b82a-4741-9d08-a17316e5cbbd",
          "name": "getMetadataTssites",
          "request": {
            "url": "http://firebrowse.org/api/v1/Metadata/TSSites?format=%7B%7D&tss_code=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "By default this function returns a table of all sites which contributed source tissue to TCGA, aka TSS's. A subset of this table may be obtained by explicitly specifying one or more sites."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a4ff6721-85e5-44c5-adc9-4ba34e23d31c"
            }
          ]
        }
      ]
    },
    {
      "name": "Samples",
      "item": [
        {
          "id": "63540bcb-f6a8-47ba-b4a1-fe800951db2d",
          "name": "getSamplesClinical",
          "request": {
            "url": "http://firebrowse.org/api/v1/Samples/Clinical?cde_name=%7B%7D&cohort=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns patient clinical data from TCGA, verbatim. It differs from the Samples/Clinical_FH method by providing access to all TCGA CDEs in their original form, not merely the subset of CDEs normalized by Firehose for analyses.  Results may be selected by disease cohort, patient barcode or CDE name, but at least one cohort, barcode, or CDE must be provided. When filtering by CDE note that only when a patient record contains one or more of the selected CDEs will it be returned. Visit the Metadata/ClinicalNames api function to see the entire list of TCGA CDEs that may be queried via this method. For more information on how clinical data are processed, see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ce3740d4-1bb0-4e5e-b26b-360661c1ff56"
            }
          ]
        }
      ]
    }
  ]
}