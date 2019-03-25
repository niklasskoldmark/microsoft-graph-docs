
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var mentions = new List<Mentions>();
mentions.Add(new Mentioned());


var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var message = new Message
{
	Subject = "Party planning",
	ToRecipients = toRecipients,
	Mentions = mentions,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(message);

```