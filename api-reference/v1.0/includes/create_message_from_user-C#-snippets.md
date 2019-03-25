
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var body = new Body
{
	ContentType = "HTML",
	Content = "They were <b>awesome</b>!",
};

var message = new Message
{
	Subject = "Did you see last night's game?",
	Importance = "Low",
	Body = body,
	ToRecipients = toRecipients,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(message);

```