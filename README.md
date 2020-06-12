# dosa-admin-client

## How to use

Document: [DosaAdminApi](https://cozou.github.io/dosa-admin-client/docs/DosaAdminApi.html)

Example:

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

## Build

**直接コード修正を行わない**

クライアントは [dosa-admin-openapi-schema](https://github.com/cozou/dosa-admin-openapi-schema) より `openapi-generator-cli` で自動生成する
