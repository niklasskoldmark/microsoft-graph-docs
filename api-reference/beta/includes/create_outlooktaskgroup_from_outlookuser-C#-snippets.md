
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var taskGroup = new TaskGroup
{
	Name = "Leisure tasks",
};

await graphClient.Me.Outlook.TaskGroups
	.Request()
	.AddAsync(taskGroup);

```