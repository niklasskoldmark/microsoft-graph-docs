
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var serie = new Serie
{
	Name = "name-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series
	.Request()
	.AddAsync(serie);

```