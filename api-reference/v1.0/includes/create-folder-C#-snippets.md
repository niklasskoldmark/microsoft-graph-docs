
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var folder = new Folder
{
};

var childre = new Childre
{
	Name = "New Folder",
	Folder = folder,
	@microsoft.graph.conflictBehavior = "rename",
};

await graphClient.Me.Drive.Root.Children
	.Request()
	.AddAsync(childre);

```