## Analytics & Integration

<img
  alt="Multi-source/multi-destination analytics, fanning-in to a Kinesis stream and fanning-out to multiple target systems"
  src="images/large-analytics-before.svg"></img>

Note:
 - Simple architecture
 - Mostly serverless
 - Rapid scaleup from 0 to x00,000 users


Issues
 - Big (1000 line plus) Lambdas to start with
 - Kinesis Java SDK feature - doesn't error when records lost, just says in the response
 - Kinesis partitions dictate lambda scaling, cost per hour to run, and don't autoscale
 - DynamoDB costs per hour to run and didn't autoscale
 - "Upsert" implemented as multiple round-trips
 - Split out into "components" of related functions and their infrastructure
 - Repos mirrored components
 - Repos contained relevant CloudFormation templates
 - Commonly used functions split out into a shared library
 - CloudFormation was crucial - "templates"
 - No visualisation - so CloudWatch dashboards covering throughput at key points
 - Default logging to CloudWatch - some debate as to whether this was good enough - no way to trace a message
 - Clojure - cold start problem https://juxt.pro/blog/posts/clojure-in-sky-bet.html
 - Testing
 - Capacity issues ground things to a halt very quickly
 - permissions - fine-grained more work but documents what's doing what to what
