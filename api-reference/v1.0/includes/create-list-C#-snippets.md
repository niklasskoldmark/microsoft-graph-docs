
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var list = new List
{
	Template = "genericList",
};

var columns = new List<Columns>();
columns.Add(new Name());
columns.Add(new Text());
columns.Add(new Name());
columns.Add(new Number());


var list = new List
{
	Name = "Books",
	Columns = columns,
	List = list,
};

await graphClient.Sites["{site-id}"].Lists
	.Request()
	.AddAsync(list);

```