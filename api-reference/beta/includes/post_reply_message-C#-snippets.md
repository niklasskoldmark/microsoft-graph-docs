
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var body = new Body
{
	ContentType = "html",
	Content = "Hello World",
};

var replie = new Replie
{
	Body = body,
};

await graphClient.Teams["{id}"].Channels["{id}"].Messages["{id}"].Replies
	.Request()
	.AddAsync(replie);

```