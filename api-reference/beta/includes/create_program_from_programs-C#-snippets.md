
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var program = new Program
{
	DisplayName = "testprogram3",
	Description = "test description",
};

await graphClient.Programs
	.Request()
	.AddAsync(program);

```