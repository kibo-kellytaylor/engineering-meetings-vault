⏺ Based on my analysis, the build failure is caused by the Jenkins shared library (kibo-pipeline-shared-lib) trying to look up service type information for kibo-redshift-extractor-default, but that service type is undefined or not found in the shared library's configuration.

  Summary

  Problem: The deployment pipeline fails with:
  ERROR: Undefined service type: kibo-redshift-extractor-default

  Root Cause: The ngProjectPipeline function from kibo-pipeline-shared-lib attempts to read service metadata (including serviceType) from a library resource using KUBE_SERVICE_NAME: 'kibo-redshift-extractor-default', but cannot find the serviceType field defined for this service.

  When it happened: This started after commit bcb29a1 which restructured the Jenkinsfile to replace old redshift container services with BigQuery extractors, but the main service name remained kibo-redshift-extractor-default.

  Recommended Solutions

  Without access to the shared library configuration, here are the most likely fixes:

  1. Add SERVICE_TYPE parameter to Jenkinsfile (if supported by the shared library):
  Add KUBE_SERVICE_TYPE: 'cron' (or appropriate type) to the ngProjectPipeline() call at the top of the Jenkinsfile.
  2. Contact the DevOps/Platform team to ensure the service descriptor for kibo-redshift-extractor-default has been properly registered in the shared library with a valid serviceType.
  3. Check if a service descriptor file should exist in a shared configuration repo that defines metadata for this service.

  Would you like me to attempt solution #1 by adding a SERVICE_TYPE parameter to the Jenkinsfile? If so, what service type should it be? (Common values might be: cron, batch, worker, database-connector, etc.)