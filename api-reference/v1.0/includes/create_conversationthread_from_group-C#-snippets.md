
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var posts = new List<Posts>();
posts.Add(new Body());
posts.Add(new NewParticipants());


var thread = new Thread
{
	Topic = "New Conversation Thread Topic",
	Posts = posts,
};

await graphClient.Groups["{id}"].Threads
	.Request()
	.AddAsync(thread);

```