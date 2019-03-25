
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var color = new Color
{
};

var calendar = new Calendar
{
	Name = "name-value",
	Color = color,
};

await graphClient.Me.CalendarGroups["{id}"].Calendars
	.Request()
	.AddAsync(calendar);

```