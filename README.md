# parquet2hive
Hive import statement generator for Parquet datasets.

## Installation
```bash
pip install parquet2hive
```

## Example usage
```bash
➜  ~  parquet2hive -d s3://telemetry-test-bucket/churn/telemetry-2/
create external table churn(clientId string, sampleId int, channel string, normalizedChannel string, country string, profileCreationDate int, subsessionStartDate int, subsessionLength int, distributionId string, submissionDate string, syncConfigured boolean, syncCountDesktop int, syncCountMobile int, version string, timestamp bigint) partitioned by (ubmissionDateS3 string) stored as parquet location 's3://telemetry-test-bucket/churn/telemetry-2/';

```