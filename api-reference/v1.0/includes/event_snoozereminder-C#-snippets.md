
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var newReminderTime = new NewReminderTime
{
	DateTime = "dateTime-value",
	TimeZone = "timeZone-value",
};

await graphClient.Me.Events["{id}"]
	.snoozeReminder(newReminderTime);
	.Request()
	.PostAsync()

```