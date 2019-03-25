
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var application = new Application
{
	AllowPublicClient = true,
	DisplayName = "Display name",
};

await graphClient.Applications
	.Request()
	.AddAsync(application);

```