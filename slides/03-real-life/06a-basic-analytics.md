## Basic Analytics

<img
  alt="Basic analytics architecture. AWS CloudFront drops files in S3 which trigger a Lambda"
  src="images/basic-analytics.png"
  width="80%"></img>

Note:
 - CloudFront drops bundles of logs into an S3 bucket
 - When files arrive in S3 the lambda is triggered with the bucket name and the key
 - Couldn't write results to Elasticache because it ran on a private subnet
 - Ended up writing to DynamoDB instead, even though it was bursty
   - No autoscaling on DynamoDB at the time
 - Lambda now supports running in specified subnets
