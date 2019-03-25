
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var fields = new List<Fields>();
fields.Add(new Key());
fields.Add(new SortOn());
fields.Add(new Ascending());
fields.Add(new Color());
fields.Add(new DataOption());
fields.Add(new Icon());


var matchCase = True;

var method = "method-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Sort
	.apply(fields,matchCase,method);
	.Request()
	.PostAsync()

```