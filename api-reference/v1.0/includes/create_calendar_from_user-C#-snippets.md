
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var calendar = new Calendar
{
	Name = "Volunteer",
};

await graphClient.Me.Calendars
	.Request()
	.AddAsync(calendar);

```