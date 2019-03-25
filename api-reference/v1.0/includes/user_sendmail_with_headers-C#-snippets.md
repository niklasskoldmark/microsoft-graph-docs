
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var internetMessageHeaders = new List<InternetMessageHeaders>();
internetMessageHeaders.Add(new Name());
internetMessageHeaders.Add(new Value());
internetMessageHeaders.Add(new Name());
internetMessageHeaders.Add(new Value());


var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var body = new Body
{
	ContentType = "HTML",
	Content = "The group represents Nevada.",
};

var message = new Message
{
	Subject = "9/9/2018: concert",
	Body = body,
	ToRecipients = toRecipients,
	InternetMessageHeaders = internetMessageHeaders,
};

await graphClient.Me
	.sendMail(message,saveToSentItems);
	.Request()
	.PostAsync()

```