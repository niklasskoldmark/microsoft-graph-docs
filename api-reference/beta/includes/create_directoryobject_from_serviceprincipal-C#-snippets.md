
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new DirectoryObject
{
};

var owner = new Owner
{
	DirectoryObject = directoryObject,
};

await graphClient.ServicePrincipals["{id}"].Owners
	.Request()
	.AddAsync(owner);

```