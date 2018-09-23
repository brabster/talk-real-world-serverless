## Hackathon Reputation System

![Schematic of the architecture - similar to the slackbot architecture, but AWS DynamoDB is the backing store and there are multiple lambda functions](images/rep-architecture.png)

Note:
 - Implemented in a two-day hackathon
 - DynamoDB provides data storage
 - multiple lambda functions to serve different endpoints, GET/POST/PUT/DELETE etc.
