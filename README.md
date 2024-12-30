# MongoDB $inc Operator Bug
This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.  The `$inc` operator is intended to increment or decrement a numeric field. However, if the field does not exist, the update will fail silently, unless you use upsert option.

## Bug
The bug lies in the incorrect usage of the `$inc` operator without handling the case where the field might not exist.

## Solution
The solution involves checking if the field exists before incrementing or using the upsert option in the updateOne() function call which will create a new document if not found.
