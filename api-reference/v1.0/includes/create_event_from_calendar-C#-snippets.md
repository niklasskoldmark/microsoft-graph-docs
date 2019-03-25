
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attendees = new List<Attendees>();
attendees.Add(new EmailAddress());
attendees.Add(new Type());


var location = new Location
{
	DisplayName = "Harry's Bar",
};

var end = new End
{
	DateTime = "2019-03-15T14:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new Start
{
	DateTime = "2019-03-15T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new Body
{
	ContentType = "HTML",
	Content = "Does mid month work for you?",
};

var event = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Calendars["AAMkAGViNDU7zAAAAAGtlAAA="].Events
	.Request()
	.AddAsync(event);

```