<!-- Start SDK Example Usage [usage] -->
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
<!-- End SDK Example Usage [usage] -->