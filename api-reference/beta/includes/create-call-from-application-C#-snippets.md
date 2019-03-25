
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var targets = new List<Targets>();
targets.Add(new Identity());


var application = new Application
{
	Id = "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698",
};

var identity = new Identity
{
	Application = application,
};

var source = new Source
{
	Identity = identity,
	LanguageId = "languageId-value",
	Region = "region-value",
};

var preFetchMedia = new List<PreFetchMedia>();
preFetchMedia.Add(new Uri());
preFetchMedia.Add(new ResourceId());
preFetchMedia.Add(new Uri());
preFetchMedia.Add(new ResourceId());


var mediaConfig = new MediaConfig
{
	@odata.type = "#microsoft.graph.serviceHostedMediaConfig",
	PreFetchMedia = preFetchMedia,
};

var call = new Call
{
	CallbackUri = "https://bot.contoso.com/api/calls",
	MediaConfig = mediaConfig,
	Source = source,
	Subject = "Test Call",
	Targets = targets,
	TenantId = "tenantId-value",
};

await graphClient.App.Calls
	.Request()
	.AddAsync(call);

```