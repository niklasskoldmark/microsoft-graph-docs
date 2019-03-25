
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var column = new Column
{
	Id = 99,
	Name = "name-value",
	Index = 99,
	Values = "values-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns
	.Request()
	.AddAsync(column);

```