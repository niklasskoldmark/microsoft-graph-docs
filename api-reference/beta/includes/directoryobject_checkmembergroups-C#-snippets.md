
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupIds = new List<GroupIds>();
groupIds.Add([
  "fee2c45b-915a-4a64-b130-f4eb9e75525e",
  "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
]);

await graphClient.Me
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```