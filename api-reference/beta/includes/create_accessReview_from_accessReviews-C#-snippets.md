
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var autoReviewSettings = new AutoReviewSettings
{
	NotReviewedResult = "Deny",
};

var recurrenceSettings = new RecurrenceSettings
{
	RecurrenceType = "onetime",
	RecurrenceEndType = "endBy",
	DurationInDays = 0,
	RecurrenceCount = 0,
};

var settings = new Settings
{
	MailNotificationsEnabled = true,
	RemindersEnabled = true,
	JustificationRequiredOnApproval = true,
	AutoReviewEnabled = false,
	ActivityDurationInDays = 30,
	AutoApplyReviewResultsEnabled = false,
	AccessRecommendationsEnabled = false,
	RecurrenceSettings = recurrenceSettings,
	AutoReviewSettings = autoReviewSettings,
};

var reviewers = new List<Reviewers>();
reviewers.Add(new Id());
reviewers.Add(new Id());


var reviewedEntity = new ReviewedEntity
{
	Id = "99025615-a0b1-47ec-9117-35377b10998b",
};

var accessReview = new AccessReview
{
	DisplayName = "TestReview",
	StartDateTime = "2017-02-10T00:35:53.214Z",
	EndDateTime = "2017-03-12T00:35:53.214Z",
	ReviewedEntity = reviewedEntity,
	ReviewerType = "delegated",
	BusinessFlowTemplateId = "6e4f3d20-c5c3-407f-9695-8460952bcc68",
	Description = "Sample description",
	Reviewers = reviewers,
	Settings = settings,
};

await graphClient.AccessReviews
	.Request()
	.AddAsync(accessReview);

```