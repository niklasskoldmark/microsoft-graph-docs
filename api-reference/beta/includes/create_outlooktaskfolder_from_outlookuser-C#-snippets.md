
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var taskFolder = new TaskFolder
{
	Name = "Volunteer",
};

await graphClient.Me.Outlook.TaskFolders
	.Request()
	.AddAsync(taskFolder);

```