
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var userIds = new List<UserIds>();
userIds.Add([
  "c5d0c76b-80c4-481c-be50-923cd8d680a1",
  "2a4296b3-a28a-44ba-bc66-0274b9b95851"
]);

var schedulingGroup = new SchedulingGroup
{
	DisplayName = "Cashiers",
	IsActive = true,
	UserIds = userIds,
};

await graphClient.Teams["{teamId}"].Schedule.SchedulingGroups
	.Request()
	.AddAsync(schedulingGroup);

```