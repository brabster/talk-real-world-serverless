## Monitoring

AWS Cloudwatch for:

- Logging
- Alarms (to Slack)
- Dashboard


Note:
- Out of the box logging in 1H 2017 was just about good enough; X-Ray etc should have improved on it
- Lambda "template" made it easier to ensure alarms that hit slack were set up (using a lambda)
- Alarms for when Lambdas errors, tables were throttled, etc.
- Dashboard primarily for throughput metrics
  - let us learn daily/weekly/longer patterns to spot unusual behaviour
  - included some summary metrics to sanity checking
