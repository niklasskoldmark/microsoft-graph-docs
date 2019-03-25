
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var ToRecipients = new List<ToRecipients>();
ToRecipients.Add(new EmailAddress());


var Comment = "Dana, hope you can make this meeting.";

await graphClient.Me.Events["{id}"]
	.forward(comment,toRecipients);
	.Request()
	.PostAsync()

```