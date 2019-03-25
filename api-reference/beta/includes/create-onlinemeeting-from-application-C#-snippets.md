
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var user = new User
{
	Id = "550fae72-d251-43ec-868c-373732c2704f",
};

var identity = new Identity
{
	User = user,
};

var organizer = new Organizer
{
	Identity = identity,
};

var participants = new Participants
{
	Organizer = organizer,
};

var onlineMeeting = new OnlineMeeting
{
	MeetingType = "meetNow",
	Participants = participants,
	Subject = "subject-value",
};

await graphClient.App.OnlineMeetings
	.Request()
	.AddAsync(onlineMeeting);

```