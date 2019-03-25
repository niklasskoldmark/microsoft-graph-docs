
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<GroupIds>();
groupIds.Add([
  "groupIds-value"
]);

await graphClient.Me
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```