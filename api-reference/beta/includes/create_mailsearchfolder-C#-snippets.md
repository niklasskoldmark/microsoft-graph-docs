
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var sourceFolderIDs = new List<SourceFolderIDs>();
sourceFolderIDs.Add([
  "AAMkAGVmMDEzM"
]);

var childFolder = new ChildFolder
{
	@odata.type = "microsoft.graph.mailSearchFolder",
	DisplayName = "Get MyAnalytics",
	IncludeNestedFolders = true,
	SourceFolderIDs = sourceFolderIDs,
	FilterQuery = "contains(subject, 'MyAnalytics')",
};

await graphClient.Me.MailFolders["searchfolders"].ChildFolders
	.Request()
	.AddAsync(childFolder);

```