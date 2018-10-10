## Mismatching Capacity

One function instance per Kinesis partition

...make sure functions are fast!

- Pay per partition per hour
- No autoscaling
- Can split/merge partitions
- Consider "backfill" scenario

Note:
 - Busy systems delay quiet ones
 - Autoscaling means you can insert coins to continue
   - Fixes a short burst, buys time for longer-term fixes
 - Stuff that autoscales but depends on stuff that doesn't doesn't autoscale!
 - Can roll your own autoscaling, but not pretty
 - Complex code and two DynamoDB accesses per message meant we had a slow function
 - In our design, busy systems delayed message processing for quiet systems
