
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var index = new Index
{
};

var values = new List<Values>();


await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns
	.add(index,values,name);
	.Request()
	.PostAsync()

```