
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<GroupIds>();
groupIds.Add([
  "groupIds-value"
]);

await graphClient.ServicePrincipals["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```