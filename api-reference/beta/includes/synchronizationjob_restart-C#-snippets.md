
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var criteria = new Criteria
{
	ResetScope = "ConnectorDataStore, Escrows, QuarantineState",
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{jobId}"]
	.restart(criteria);
	.Request()
	.PostAsync()

```