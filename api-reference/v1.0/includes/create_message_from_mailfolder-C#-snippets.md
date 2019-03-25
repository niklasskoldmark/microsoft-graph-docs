
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var body = new Body
{
	ContentType = "",
	Content = "content-value",
};

var message = new Message
{
	ReceivedDateTime = "datetime-value",
	SentDateTime = "datetime-value",
	HasAttachments = true,
	Subject = "subject-value",
	Body = body,
	BodyPreview = "bodyPreview-value",
};

await graphClient.Me.MailFolders["{id}"].Messages
	.Request()
	.AddAsync(message);

```