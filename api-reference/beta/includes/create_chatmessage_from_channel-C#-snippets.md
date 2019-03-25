
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var body = new Body
{
	ContentType = "html",
	Content = "Hello World",
};

var message = new Message
{
	Body = body,
};

await graphClient.Teams["{id}"].Channels["{id}"].Messages
	.Request()
	.AddAsync(message);

```