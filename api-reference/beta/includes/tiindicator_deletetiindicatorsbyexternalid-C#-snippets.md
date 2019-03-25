
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<Value>();
value.Add([
  "externalId-value1",
  "externalId-value2"
]);

await graphClient.Security.TiIndicators
	.deleteTiIndicatorsByExternalId(value);
	.Request()
	.PostAsync()

```