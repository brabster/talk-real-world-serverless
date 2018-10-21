## Testing

- Unit Testing
- Integration Testing
- End-to-End Testing

Note:
 - Unit testing was fine - just like any other code
   - ensure processing is separated so that mock inputs can be provided and outputs checked
 - Integration testing was fine where things like DynamoDB-Local exist
   - otherwise, it gets tricky, and questionable relevance if not actually running on real infra
   - don't write your own framework
   - consider consumer contracts
   - generative testing - maybe depends on contracts anyway
 - End-to-end testing
   - quotas, time to spin up, complexity
   - ended up with manual testing in a staging environment
   - but did get some sanity checks running to make sure basics were working correctly
