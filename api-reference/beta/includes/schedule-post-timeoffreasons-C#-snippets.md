
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var timeOffReason = new TimeOffReason
{
	DisplayName = "Vacation",
	IconType = "plane",
	IsActive = true,
};

await graphClient.Teams["{teamId}"].Schedule.TimeOffReasons
	.Request()
	.AddAsync(timeOffReason);

```