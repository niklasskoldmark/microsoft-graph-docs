
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new DirectoryObject
{
};

var owner = new Owner
{
	DirectoryObject = directoryObject,
};

await graphClient.Applications["{id}"].Owners
	.Request()
	.AddAsync(owner);

```