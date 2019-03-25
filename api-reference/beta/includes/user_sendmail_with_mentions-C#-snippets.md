
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var mentions = new List<Mentions>();
mentions.Add(new Mentioned());


var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var Message = new Message
{
	Subject = "Project kickoff",
	ToRecipients = toRecipients,
	Mentions = mentions,
};

await graphClient.Me
	.sendMail(message,saveToSentItems);
	.Request()
	.PostAsync()

```