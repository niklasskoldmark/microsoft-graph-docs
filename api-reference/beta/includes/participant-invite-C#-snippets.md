
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var participants = new List<Participants>();
participants.Add(new EndpointType());
participants.Add(new Identity());
participants.Add(new LanguageId());
participants.Add(new Region());
participants.Add(new ReplacesCallId());


var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants
	.invite(participants,clientContext);
	.Request()
	.PostAsync()

```