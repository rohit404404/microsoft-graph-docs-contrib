---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let alerts = await client.api('/reports/healthMonitoring/alerts')
	.version('beta')
	.get();

```