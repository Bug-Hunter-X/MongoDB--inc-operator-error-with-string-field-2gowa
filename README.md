# MongoDB $inc operator error with string field

This example demonstrates an error that can occur when using the `$inc` operator with a string field in MongoDB. The `$inc` operator is designed to increment numeric fields, not string fields.  Attempting to use it with a string will result in an error.

## Bug
The bug is caused by attempting to increment a string field using the `$inc` operator.  This is a common mistake and results in a database operation failure.

## Solution
The solution is to ensure the field being incremented is of the correct datatype (Number).  If the field currently holds a string, you need to update the field to be numeric before attempting to use the `$inc` operator. Or, If you are intending to concatenate, use `$push` or other string manipulation operators instead.