# dosa-admin-client

## How to use

```javascript
import { DosaAdminApi, Configuration } from 'dosa-admin-client';

(async () => {
  const basePath = 'http://localhost:8000';
  const config = new Configuration({ basePath });
  const client = new DosaAdminApi(config);

  const response = await client.getParticipants('user1@example.com');
  if (!response.data || !response.data.data) return;

  console.table(response.data.data);
})();
```
