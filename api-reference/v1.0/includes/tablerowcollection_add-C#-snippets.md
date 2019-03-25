
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var index = 5;

var values = new List<Values>();
values.Add([
  [
    1,
    2,
    3
  ],
  [
    4,
    5,
    6
  ]
]);

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows
	.add(index,values);
	.Request()
	.PostAsync()

```