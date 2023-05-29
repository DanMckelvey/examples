This function is part of a large reporting application used by BCTS personnel for creating custom reports based off BC Timber Sales data.
This application communicates directly to our Oracle database via SQL, but the application itself is built in MS Access.
This function is an example of combining SQL and VBA to create a dynamic query so that the user can define certain parameters.

The query is broken up into three parts, stFields, stTables, and stConditions.
These are the SELECT, FROM and WHERE portions of the SQL respectively.

For this query, the user can specify the date range, and Area Code.
Line 30 is an example of where we include another VBA function nested in the SQL.
getToDateInString() is the fucntion that retrieves a user submited data for this query.
