
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var job = new Job
{
	TemplateId = "BoxOutDelta",
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs
	.Request()
	.AddAsync(job);

```