
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var point = new Point
{
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series["{series-id}"].Points
	.Request()
	.AddAsync(point);

```