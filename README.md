# snowflake-to-cloudwatch
## Code for monitoring Snowflake with AWS CloudWatch

Basic setup

1. Install the AWS CLI
2. Run `aws configure`. Configure the CLI with an account that has appropriate permissions to CloudWatch.
3. Install Snowsql.
4. Edit the Snowsql config file `~/.snowsql/config`. You will need to set username, password, account and warehouse.
5. Test the Snowsql CLI by running `snowsql -f metric_sql_script`.
6. Edit the SQL in `metric-sql-script` to point to your warehouse.
7. Edit `monitoring-script` to point to the `metric-name` and `namespace` of your choice.
8. To write current metrics, run `./monitoring-script`.
9. Consider moving Snowsql to key pair authentication for a production use case.
