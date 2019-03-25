
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var childFolder = new ChildFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.ContactFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolder);

```