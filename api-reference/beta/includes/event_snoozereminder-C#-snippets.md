
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var newReminderTime = new NewReminderTime
{
	DateTime = "2016-10-19T10:37:00Z",
	TimeZone = "timeZone-value",
};

await graphClient.Me.Events["{id}"]
	.snoozeReminder(newReminderTime);
	.Request()
	.PostAsync()

```