
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var threads = new List<Threads>();
threads.Add(new Posts());


var conversation = new Conversation
{
	Topic = "New locations for this quarter",
	Threads = threads,
};

await graphClient.Groups["29981b6a-0e57-42dc-94c9-cd24f5306196"].Conversations
	.Request()
	.AddAsync(conversation);

```