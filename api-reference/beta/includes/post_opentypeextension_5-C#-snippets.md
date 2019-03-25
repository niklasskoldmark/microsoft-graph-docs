
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var Threads = new List<Threads>();
Threads.Add(new Posts());


var conversation = new Conversation
{
	Topic = "Does anyone have a second?",
	Threads = Threads,
};

await graphClient.Groups["37df2ff0-0de0-4c33-8aee-75289364aef6"].Conversations
	.Request()
	.AddAsync(conversation);

```