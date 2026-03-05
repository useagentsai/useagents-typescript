# Validation

## Example Usage

```typescript
import { Validation } from "@useagents/sdk/models";

let value: Validation = {
  field: "q",
  message: "Required",
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  | Example                                      |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `field`                                      | *string*                                     | :heavy_check_mark:                           | The name of the field that failed validation | q                                            |
| `message`                                    | *string*                                     | :heavy_check_mark:                           | The validation error message for the field   | Required                                     |