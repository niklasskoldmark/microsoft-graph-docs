
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var locations = new List<Locations>();
locations.Add(new DisplayName());
locations.Add(new DisplayName());
locations.Add(new Address());
locations.Add(new Coordinates());
locations.Add(new DisplayName());


var location = new Location
{
	DisplayName = "Conf Room 3; Fourth Coffee; Home Office",
	LocationType = "Default",
};

var attendees = new List<Attendees>();
attendees.Add(new EmailAddress());
attendees.Add(new Type());
attendees.Add(new EmailAddress());
attendees.Add(new Type());


var end = new End
{
	DateTime = "2017-08-30T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new Start
{
	DateTime = "2017-08-30T11:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new Body
{
	ContentType = "HTML",
	Content = "Let's kick-start this event planning!",
};

var event = new Event
{
	Subject = "Plan summer company picnic",
	Body = body,
	Start = start,
	End = end,
	Attendees = attendees,
	Location = location,
	Locations = locations,
};

await graphClient.Me.Events
	.Request()
	.AddAsync(event);

```