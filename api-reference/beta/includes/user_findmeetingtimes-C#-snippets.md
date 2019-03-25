
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attendees = new List<Attendees>();
attendees.Add(new Type());
attendees.Add(new EmailAddress());


var locations = new List<Locations>();
locations.Add(new ResolveAvailability());
locations.Add(new DisplayName());


var locationConstraint = new LocationConstraint
{
	IsRequired = "false",
	SuggestLocation = "false",
	Locations = locations,
};

var timeslots = new List<Timeslots>();
timeslots.Add(new Start());
timeslots.Add(new End());


var timeConstraint = new TimeConstraint
{
	ActivityDomain = "work",
	Timeslots = timeslots,
};

var isOrganizerOptional = "false";

var meetingDuration = "PT1H";

var returnSuggestionReasons = "true";

var minimumAttendeePercentage = "100";

await graphClient.Me
	.findMeetingTimes(attendees,locationConstraint,timeConstraint,meetingDuration,maxCandidates,isOrganizerOptional,returnSuggestionReasons,minimumAttendeePercentage);
	.Request()
	.PostAsync()

```