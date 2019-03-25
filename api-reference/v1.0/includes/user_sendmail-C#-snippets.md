
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var ccRecipients = new List<CcRecipients>();
ccRecipients.Add(new EmailAddress());


var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var body = new Body
{
	ContentType = "Text",
	Content = "The new cafeteria is open.",
};

var message = new Message
{
	Subject = "Meet for lunch?",
	Body = body,
	ToRecipients = toRecipients,
	CcRecipients = ccRecipients,
};

var saveToSentItems = "false";

await graphClient.Me
	.sendMail(message,saveToSentItems);
	.Request()
	.PostAsync()

```