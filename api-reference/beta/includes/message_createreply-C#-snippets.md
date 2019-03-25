
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());
toRecipients.Add(new EmailAddress());


var message = new Message
{
	ToRecipients = toRecipients,
};

var comment = "Samantha, Randi, would you name the group if the project is approved, please?";

await graphClient.Me.Messages["AAMkADA1MTAAAAqldOAAA="]
	.createReply(message,comment);
	.Request()
	.PostAsync()

```