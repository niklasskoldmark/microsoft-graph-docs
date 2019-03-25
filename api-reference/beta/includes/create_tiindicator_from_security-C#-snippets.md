
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var tags = new List<Tags>();
tags.Add([]);

var malwareFamilyNames = new List<MalwareFamilyNames>();
malwareFamilyNames.Add([]);

var killChain = new List<KillChain>();
killChain.Add([]);

var activityGroupNames = new List<ActivityGroupNames>();
activityGroupNames.Add([]);

var tiIndicator = new TiIndicator
{
	Action = "alert",
	ActivityGroupNames = activityGroupNames,
	Confidence = 0,
	Description = "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.",
	ExpirationDateTime = "2019-03-02T00:43:37.5031462+03:00",
	ExternalId = "Test--8586509942679764298MS501",
	FileHashType = "sha256",
	FileHashValue = "aa64428647b57bf51524d1756b2ed746e5a3f31b67cf7fe5b5d8a9daf07ca313",
	KillChain = killChain,
	MalwareFamilyNames = malwareFamilyNames,
	Severity = 0,
	Tags = tags,
	TargetProduct = "Azure Sentinel",
	ThreatType = "WatchList",
	TlpLevel = "green",
};

await graphClient.Security.TiIndicators
	.Request()
	.AddAsync(tiIndicator);

```