
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var comment = "comment-value";

var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"]
	.forward(comment,toRecipients);
	.Request()
	.PostAsync()

```