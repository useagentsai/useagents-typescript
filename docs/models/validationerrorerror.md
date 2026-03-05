# ValidationErrorError

## Example Usage

```typescript
import { ValidationErrorError } from "@useagents/sdk/models";

let value: ValidationErrorError = {
  status: 422,
  code: "validation_error",
  message: "We found an error with one or more fields in the request.",
  validation: [
    {
      field: "q",
      message: "Required",
    },
  ],
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               | Example                                                   |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `status`                                                  | *number*                                                  | :heavy_check_mark:                                        | HTTP status code of the error                             | 422                                                       |
| `code`                                                    | *string*                                                  | :heavy_check_mark:                                        | Machine-readable error name                               | validation_error                                          |
| `message`                                                 | *string*                                                  | :heavy_check_mark:                                        | Human-readable error message                              | We found an error with one or more fields in the request. |
| `validation`                                              | [models.Validation](../models/validation.md)[]            | :heavy_check_mark:                                        | List of field-specific validation issues                  |                                                           |