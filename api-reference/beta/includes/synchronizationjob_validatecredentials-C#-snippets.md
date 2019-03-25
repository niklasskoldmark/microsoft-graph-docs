
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var credentials = new List<Credentials>();
credentials.Add(new Key());
credentials.Add(new Value());
credentials.Add(new Key());
credentials.Add(new Value());


await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{id}"]
	.validateCredentials(applicationIdentifier,templateId,useSavedCredentials,credentials);
	.Request()
	.PostAsync()

```