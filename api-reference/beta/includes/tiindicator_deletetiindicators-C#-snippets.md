
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<Value>();
value.Add([
  "id-value1",
  "id-value2"
]);

await graphClient.Security.TiIndicators
	.deleteTiIndicators(value);
	.Request()
	.PostAsync()

```