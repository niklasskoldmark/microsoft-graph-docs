
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var contactFolder = new ContactFolder
{
	ParentFolderId = "parentFolderId-value",
	DisplayName = "displayName-value",
};

await graphClient.Me.ContactFolders
	.Request()
	.AddAsync(contactFolder);

```