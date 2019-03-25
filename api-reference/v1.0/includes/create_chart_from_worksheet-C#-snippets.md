
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var chart = new Chart
{
	Id = "id-value",
	Height = 99,
	Left = 99,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts
	.Request()
	.AddAsync(chart);

```