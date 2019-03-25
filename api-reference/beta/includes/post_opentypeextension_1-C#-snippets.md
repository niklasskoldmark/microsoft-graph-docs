
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var extensions = new List<Extensions>();
extensions.Add(new @odata.type());
extensions.Add(new ExtensionName());
extensions.Add(new CompanyName());
extensions.Add(new ExpirationDate());
extensions.Add(new DealValue());


var toRecipients = new List<ToRecipients>();
toRecipients.Add(new EmailAddress());


var body = new Body
{
	ContentType = "HTML",
	Content = "You should be proud!",
};

var message = new Message
{
	Subject = "Annual review",
	Body = body,
	ToRecipients = toRecipients,
	Extensions = extensions,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(message);

```