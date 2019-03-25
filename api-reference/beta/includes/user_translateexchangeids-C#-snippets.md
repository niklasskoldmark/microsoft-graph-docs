
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var inputIds = new List<InputIds>();
inputIds.Add([
  "{rest-formatted-id-1}",
  "{rest-formatted-id-2}"
]);

var sourceIdType = "restId";

var targetIdType = "restImmutableEntryId";

await graphClient.Me
	.translateExchangeIds(inputIds,targetIdType,sourceIdType);
	.Request()
	.PostAsync()

```