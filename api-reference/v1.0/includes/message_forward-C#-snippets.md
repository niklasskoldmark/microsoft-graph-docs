
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var comment = "comment-value";

var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


await graphClient.Me.Messages["{id}"]
	.forward(comment,toRecipients);
	.Request()
	.PostAsync()

```