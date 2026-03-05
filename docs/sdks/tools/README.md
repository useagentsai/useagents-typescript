# Tools
(*tools*)

## Overview

Search and discover AI agent tools

### Available Operations

* [search](#search) - Search tools

## search

Search for AI agent tools by query. Returns JSON results.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchTools" method="get" path="/tools/search" -->
```typescript
import { UseAgents } from "@useagents/sdk";

const useAgents = new UseAgents();

async function run() {
  const result = await useAgents.tools.search({
    q: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { UseAgentsCore } from "@useagents/sdk/core.js";
import { toolsSearch } from "@useagents/sdk/funcs/toolsSearch.js";

// Use `UseAgentsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const useAgents = new UseAgentsCore();

async function run() {
  const res = await toolsSearch(useAgents, {
    q: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("toolsSearch failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchToolsRequest](../../models/operations/searchtoolsrequest.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchToolsResponse](../../models/operations/searchtoolsresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.MissingApiKeyError     | 401                           | application/json              |
| errors.InvalidApiKeyError     | 403                           | application/json              |
| errors.NotFoundError          | 404                           | application/json              |
| errors.MethodNotAllowedError  | 405                           | application/json              |
| errors.ValidationError        | 422                           | application/json              |
| errors.RateLimitExceededError | 429                           | application/json              |
| errors.InternalServerError    | 500                           | application/json              |
| errors.UseAgentsDefaultError  | 4XX, 5XX                      | \*/\*                         |