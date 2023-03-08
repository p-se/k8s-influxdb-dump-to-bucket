# Container to dump InfluxDB database to AWS bucket

## Requirements

- An pre-existing S3 bucket (or the instructions in job.yaml need to be adapted)
- AWS credentials to use to access the S3 bucket

### Environment variables

#### InfluxDB

- `INFLUXDB_HOST` (also contains the port, separated by a colon)

Note that `influxd` is used to create the backup, not `influx`. Compared to
`influx`, `influxd` does not require nor allow credentials to be used and needs
to connect to a different port than `influx`. By default `influx` connects to
port `8086`, whereas `influxd` connects to port `8088`.

#### AWS

- `BUCKET_NAME`
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_DEFAULT_REGION`
