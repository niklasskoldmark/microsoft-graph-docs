
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var dueDateTime = new DueDateTime
{
	DateTime = "2016-05-05T16:00:00",
	TimeZone = "Eastern Standard Time",
};

var startDateTime = new StartDateTime
{
	DateTime = "2016-05-03T09:00:00",
	TimeZone = "Eastern Standard Time",
};

var task = new Task
{
	AssignedTo = "Dana Swope",
	Subject = "Shop for children's weekend",
	StartDateTime = startDateTime,
	DueDateTime = dueDateTime,
};

await graphClient.Me.Outlook.Tasks
	.Request()
	.AddAsync(task);

```