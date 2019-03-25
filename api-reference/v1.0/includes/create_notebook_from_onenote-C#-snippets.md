
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var notebook = new Notebook
{
	DisplayName = "Notebook name",
};

await graphClient.Me.Onenote.Notebooks
	.Request()
	.AddAsync(notebook);

```