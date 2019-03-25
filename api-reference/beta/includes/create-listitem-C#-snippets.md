
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var fields = new Fields
{
	Title = "Widget",
	Color = "Purple",
	Weight = 32,
};

var item = new Item
{
	Fields = fields,
};

await graphClient.Sites["{site-id}"].Lists["{list-id}"].Items
	.Request()
	.AddAsync(item);

```