
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var user = new User
{
	Id = "550fae72-d251-43ec-868c-373732c2704f",
	TenantId = "72f988bf-86f1-41af-91ab-2d7cd011db47",
	DisplayName = "Heidi Steen",
};

var identity = new Identity
{
	User = user,
};

var transferTarget = new TransferTarget
{
	EndpointType = "default",
	Identity = identity,
	LanguageId = "languageId-value",
	Region = "region-value",
	ReplacesCallId = "replacesCallId-value",
};

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"]
	.transfer(transferTarget,target,replacesCallId);
	.Request()
	.PostAsync()

```