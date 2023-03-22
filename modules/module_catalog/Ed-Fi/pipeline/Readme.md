# Master Pipeline
The master Pipeline is the main Orchestrator pipeline for the Ed-Fi Module, which will trigger the Ed-Fi resources and OEA framework resources and processes the Ed-Fi data end-to-end
The main pipeline has 3 major components:

1. Landing Ed-Fi Data (All tables and descriptors) incrementally from all the Ed-Fi Instances into ADLS in stage1 container as JSON format. This done by invoking Ed-Fi REST API through the Copy Activity tool to Copy data into the ADLS.

2. Ingest the data from Stage1 to Stage2 in Delta format and also do necessary transformations using Dataflows into Ingested folder.

3. Run PySpark Notebook "Refine_EdFi" which will add the necessary schema information, flattens and pseodynimizes the ingested data and writes it to Refined Folder in stage2.

4. Create SQL Serverless databases and Views in the workspace.

# OEA Dependencies
1) Pipelines:
   - Copy data from REST API to ADLS
   - Setup Database from New Stages
2) Datasets:
   - DS_REST
   - DS_JSON
   - DS_JSON_file
3) Linked Services:
   - LS_HTTP
   - LS_KeyVault
   - LS_SQL_Serverless_OEA

# Note
1) The Azure synapse workspace you are working in, should have the managed identity Storage Blob Data Contributor permission to the Storage account we are trying to connect. You must add this policy in the Access Control section in the respective Storage account. Failing to do so might lead to a 403 (Forbidden) error.
2)
