
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attendees = new List<Attendees>();
attendees.Add(new EmailAddress());
attendees.Add(new Type());


var location = new Location
{
	DisplayName = "Harry's Bar",
};

var range = new Range
{
	Type = "endDate",
	StartDate = "2017-09-04",
	EndDate = "2017-12-31",
};

var daysOfWeek = new List<DaysOfWeek>();
daysOfWeek.Add([
  "Monday"
]);

var pattern = new Pattern
{
	Type = "weekly",
	Interval = 1,
	DaysOfWeek = daysOfWeek,
};

var recurrence = new Recurrence
{
	Pattern = pattern,
	Range = range,
};

var end = new End
{
	DateTime = "2017-09-04T14:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new Start
{
	DateTime = "2017-09-04T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new Body
{
	ContentType = "HTML",
	Content = "Does noon time work for you?",
};

var event = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Recurrence = recurrence,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Events
	.Request()
	.AddAsync(event);

```