{
  "info": {
    "name": "Fire Browse Beta API Retrieve mRNASeq data.",
    "_postman_id": "c0e1241e-82aa-4465-adc0-de9f0d5d0923",
    "description": "This service returns sample-level log2 mRNASeq expression values. Results may be filtered by gene, cohort, barcode, sample type or characterization protocol, but at least one gene must be supplied.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "8bb78bbb-a1cb-43fd-ac58-f457e5bc0bb7",
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
              "id": "07eb33d8-bd40-47d2-a342-25c863e43380"
            }
          ]
        },
        {
          "id": "91dffa03-5812-49c3-9941-b9902d78395a",
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
              "id": "a64ed099-45a7-4d0e-9ce4-45ee5e2de7fa"
            }
          ]
        },
        {
          "id": "e4e1535e-b2a9-42ba-a4a4-4a4ae20242a6",
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
              "id": "133412c7-d493-455f-9238-db017561f0fe"
            }
          ]
        },
        {
          "id": "fb3c2ef9-cf16-4f7b-836f-155722844275",
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
              "id": "934c1059-af01-46ba-9d81-acd173893f2f"
            }
          ]
        },
        {
          "id": "993b5c6b-3507-402a-aab1-4621aee69d82",
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
              "id": "4ec88d0d-4cd4-46db-a2b7-613647cb8b37"
            }
          ]
        },
        {
          "id": "d7c4ba70-7319-4c02-ba1c-20f22bf44642",
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
              "id": "a7183c8c-dd5a-4cfd-b9e8-296f4e94441e"
            }
          ]
        },
        {
          "id": "795bb0ba-7ef3-4022-a9a8-bb6dc640220a",
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
              "id": "606a6be1-22e9-4cd7-b4c6-138497b6ef84"
            }
          ]
        },
        {
          "id": "05b6aedf-4f81-43c1-967b-06756f3a3bff",
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
              "id": "de60609c-a288-4c1a-8e8f-49cb03e4b724"
            }
          ]
        },
        {
          "id": "730470ca-3554-4fa0-adcc-73059582ba90",
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
              "id": "d244bec9-b26f-461a-89a9-021c022d195f"
            }
          ]
        },
        {
          "id": "41ba9fac-95c1-41e0-8d1c-e1d8be20ace1",
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
              "id": "d919552d-7a7f-4cc9-ba73-a5c621be864c"
            }
          ]
        }
      ]
    },
    {
      "name": "Archives",
      "item": [
        {
          "id": "648afe40-c572-4aac-9d9e-bbe1bd2c4489",
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
              "id": "80d4b3df-01c3-41cf-b92e-f371c63aa0c2"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadata",
      "item": [
        {
          "id": "61da116b-954d-4ef4-b90c-4b6dd4d79c03",
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
              "id": "2dd9b05a-493c-42fe-b2fa-36991d437a78"
            }
          ]
        },
        {
          "id": "5fdddffa-6f7e-4fee-baa5-df1b52f720ec",
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
              "id": "95e64e50-50ad-4949-9ad2-14f79cac2c6d"
            }
          ]
        },
        {
          "id": "88044c30-7f1b-4e8f-98f6-ba48bfc74b2e",
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
              "id": "140568dc-599f-431d-8096-3356d48e91b1"
            }
          ]
        },
        {
          "id": "9866c6b6-1b58-4493-a3c4-e8fde736cf65",
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
              "id": "2aaca8ea-6f8f-424b-ac85-793d3e70aa05"
            }
          ]
        },
        {
          "id": "b8c8df7d-2c91-4c8a-921d-e87df4dccede",
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
              "id": "e6cbe94c-13bc-4a5f-b15c-ef1fe95d1de6"
            }
          ]
        },
        {
          "id": "c6f98fa3-e6f9-41dd-bf88-c676391657f4",
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
              "id": "0f1b06b4-aeb4-4b9f-afca-d8ccb576f18e"
            }
          ]
        },
        {
          "id": "892d0c36-e38b-449f-9366-83685cf04e59",
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
              "id": "d7e568f2-f241-49af-8947-3eb97d68f520"
            }
          ]
        },
        {
          "id": "6baba7ce-a7c8-4eb6-a6ed-9e2902da2a7c",
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
              "id": "9bf65158-60eb-4193-a29c-946a930e314b"
            }
          ]
        },
        {
          "id": "b7e41aff-dcc8-4684-a0ff-f0825ffdb089",
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
              "id": "7442e890-b284-42da-b6c5-eb512098ebb2"
            }
          ]
        },
        {
          "id": "ae3aa6b3-8c80-4bcc-905d-bca091c2b69b",
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
              "id": "527a11f5-b8cd-4230-a1d1-18cfa96ff20f"
            }
          ]
        },
        {
          "id": "f911d6fa-9865-4b06-9b42-52080656bfc9",
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
              "id": "743cbb8f-0c84-47e8-ac9d-b9b4d63f729c"
            }
          ]
        },
        {
          "id": "d5931b76-a3ee-465f-9bf6-29dbfe943b96",
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
              "id": "8de6aebb-56b9-4444-a94c-c94a0b2e9bfe"
            }
          ]
        },
        {
          "id": "668d5983-4714-4729-9325-829e4384788c",
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
              "id": "c4457f62-b150-40de-af6d-940b42d07ca6"
            }
          ]
        },
        {
          "id": "d0a562da-7166-485d-93f2-72845f00572b",
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
              "id": "63aad811-6dfb-4103-9ae0-5cbcf5d7fa8b"
            }
          ]
        },
        {
          "id": "31425035-d128-40cf-a254-febb9facca57",
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
              "id": "682f2c0b-54e3-415d-9d70-063f18634af0"
            }
          ]
        }
      ]
    },
    {
      "name": "Samples",
      "item": [
        {
          "id": "286d4032-9c96-4136-baa9-b7d0bba66ddf",
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
              "id": "0d1083a6-6ca0-4189-9199-1cea3d7cfb9d"
            }
          ]
        },
        {
          "id": "74462a57-9c4c-4f54-add9-848de65c7060",
          "name": "getSamplesClinicalFh",
          "request": {
            "url": "http://firebrowse.org/api/v1/Samples/Clinical_FH?cohort=%7B%7D&fh_cde_name=%7B%7D&format=%7B%7D&page=%7B%7D&page_size=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns patient-level clinical data elements (CDEs) that have been normalized by Firehose for use in analyses. Results may be selected by disease cohort, patient barcode or CDE name, but at least one cohort, barcode or CDE must be provided. When filtering by CDE note that only when a  patient record contains one or more of the selected CDEs will it be returned. Visit this table of CDEs to see what's available for every disase cohort; for more information on how these CDEs are processed see our pipeline documentation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9497da68-3c85-453a-93ed-440222c3ea9d"
            }
          ]
        },
        {
          "id": "50ebf4f6-410d-4a7f-945c-c9ed3d4c43f6",
          "name": "getSamplesMrnaseq",
          "request": {
            "url": "http://firebrowse.org/api/v1/Samples/mRNASeq?cohort=%7B%7D&format=%7B%7D&gene=%7B%7D&page=%7B%7D&page_size=%7B%7D&protocol=%7B%7D&sample_type=%7B%7D&sort_by=%7B%7D&tcga_participant_barcode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service returns sample-level log2 mRNASeq expression values. Results may be filtered by gene, cohort, barcode, sample type or characterization protocol, but at least one gene must be supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ec7ccb7-cd93-4b5e-a255-b4738b546147"
            }
          ]
        }
      ]
    }
  ]
}