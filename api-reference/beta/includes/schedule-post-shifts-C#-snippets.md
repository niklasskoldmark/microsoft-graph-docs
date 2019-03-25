
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var activities = new List<Activities>();
activities.Add(new IsPaid());
activities.Add(new StartDateTime());
activities.Add(new EndDateTime());
activities.Add(new Code());
activities.Add(new DisplayName());


var draftShift = new DraftShift
{
	DisplayName = "Day shift",
	Notes = "Please do inventory as part of your shift.",
	StartDateTime = "2019-03-11T15:00:00Z",
	EndDateTime = "2019-03-12T00:00:00Z",
	Theme = "blue",
	Activities = activities,
};

var activities = new List<Activities>();
activities.Add(new IsPaid());
activities.Add(new StartDateTime());
activities.Add(new EndDateTime());
activities.Add(new Code());
activities.Add(new DisplayName());


var sharedShift = new SharedShift
{
	DisplayName = "Day shift",
	Notes = "Please do inventory as part of your shift.",
	StartDateTime = "2019-03-11T15:00:00Z",
	EndDateTime = "2019-03-12T00:00:00Z",
	Theme = "blue",
	Activities = activities,
};

var shift = new Shift
{
	Id = "SHFT_577b75d2-a927-48c0-a5d1-dc984894e7b8",
	UserId = "c5d0c76b-80c4-481c-be50-923cd8d680a1",
	SchedulingGroupId = "TAG_228940ed-ff84-4e25-b129-1b395cf78be0",
	SharedShift = sharedShift,
	DraftShift = draftShift,
};

await graphClient.Teams["{teamId}"].Schedule.Shifts
	.Request()
	.AddAsync(shift);

```