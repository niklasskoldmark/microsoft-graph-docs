
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<Value>();
value.Add(new Id());
value.Add(new AdditionalInformation());
value.Add(new Id());
value.Add(new AdditionalInformation());


await graphClient.Security.TiIndicators
	.updateTiIndicators(value);
	.Request()
	.PostAsync()

```