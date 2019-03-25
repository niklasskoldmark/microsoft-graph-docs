
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var childFolder = new ChildFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolder);

```