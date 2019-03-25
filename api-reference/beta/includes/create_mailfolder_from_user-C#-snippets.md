
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var mailFolder = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders
	.Request()
	.AddAsync(mailFolder);

```