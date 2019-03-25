
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var posts = new List<Posts>();
posts.Add(new Body());


var thread = new Thread
{
	Topic = "topic-value",
	Posts = posts,
};

await graphClient.Groups["{id}"].Conversations["{id}"].Threads
	.Request()
	.AddAsync(thread);

```