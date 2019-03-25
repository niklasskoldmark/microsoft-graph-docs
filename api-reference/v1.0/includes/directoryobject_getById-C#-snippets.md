
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var ids = new List<Ids>();
ids.Add([
  "84b80893874940a3-97b7-68513b600544",
  "5d6059b6368d-45f8-91e18e07d485f1d0"
]);

var types = new List<Types>();
types.Add([
  "user"
]);

await graphClient.DirectoryObjects
	.getByIds(ids,types);
	.Request()
	.PostAsync()

```