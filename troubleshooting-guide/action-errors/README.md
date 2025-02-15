# Action Errors

![Click to expand](../../.gitbook/assets/timeout-error.png)

### Timeout Error

If your API / DB Query times out, it could be due to one of the following reasons

* Your API / Database is behind a VPC which is not accessible from the appsmith Instance. This can be fixed by

  [whitelisting the appsmith instance](../../core-concepts/connecting-to-data-sources/) in your database or VPC.

* Your API / Query is taking too long to respond. This can be fixed by fetching smaller datasets using

[server-side pagination](../../core-concepts/displaying-data-read/display-data-tables.md#pagination) or increasing the timeout of the API / Query in the [settings section](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database).

### Configuration Error

```text
getUsers failed to execute. Please check it's configuration
```

This message indicates an error in the configuration of the action. You can navigate to the [API](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) / [Query](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) in this state and see the error it encountered. If the error occurred intermittently, it is likely due to a value in the configuration not being available at the time that the API / Query was run.

### Mandatory Parameter Empty Error

```text
Mandatory parameters 'Action' and 'Bucket Name' are missing
```

```text
Required parameter 'File Path' is missing
```

```text
Missing action name (like `ListTables`, `GetItem` etc.)
```

```text
Document/Collection path cannot be empty
```

```text
Missing Firestore method
```

A message of this type means that at least one of the mandatory / required fields in the query editor form is missing.

This error can be fixed by editing the [query editor form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) and providing the parameter mentioned in the error message.

### Missing Query Error

```text
Missing required parameter: Query
```

```text
needs a non-empty body to work
```

```text
Body is null or empty
```

Any one of these messages indicated that the body of the query has been left empty.

This error can be fixed by editing the [query form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) and providing a query body.

### Invalid Query Error

```text
Not a valid Redis command
```

```text
Query preparation failed while inserting value
```

A message of this type indicates that the syntax of the query body is invalid.

This error can be fixed by providing a valid syntax in the [query editor form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database).

### Encoding Error

```text
File content is not base64 encoded
```

This message indicates that the query was expecting a [base64 encoded](https://en.wikipedia.org/wiki/Base64) value as content body, but the actual value passed to it was not base64 encoded.

This error can be fixed by passing a base64 encoded value as file content parameter in the query.

### Invalid Number Error

```text
Parameter 'Expiry Duration of Signed URL' is NOT a number
```

This message indicates that the query parameter mentioned in the message expects a number but a non-numerical value has been provided in the [query form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database).

This error can be fixed by editing the [query form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) and providing a valid number as input for the mentioned parameter.

### JSON Parsing Error

```text
Error parsing the JSON body
```

```text
Error converting array to ND-JSON
```

```text
Unable to parse condition value as a JSON list
```

This message indicates that the [JSON](https://www.w3schools.com/whatis/whatis_json.asp#:~:text=JSON%20stands%20for%20JavaScript%20Object,describing%22%20and%20easy%20to%20understand) string passed to the query as a parameter is not a valid JSON string.

This error can be fixed by editing the [query form](https://docs.appsmith.com/core-concepts/connecting-to-data-sources/querying-a-database) and passing a valid JSON string as a parameter.

