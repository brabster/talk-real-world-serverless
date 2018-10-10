## Production Glue

![DynamoDB producing a stream of updates that Lambda transforms and pushes into Elasticsearch](images/glue-code.png)

Note:
 - DynamoDB can produce a stream of changes
 - Lambda can use the stream as a trigger
 - Updates in DynamoDB can be synchronised elsewhere without servers
 - Needed to authenticate to Elasticsearch outside of AWS IAM
