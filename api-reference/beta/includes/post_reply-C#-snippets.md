
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new List<Attachments>();
attachments.Add(new LastModifiedDateTime());
attachments.Add(new Name());
attachments.Add(new ContentType());
attachments.Add(new Size());
attachments.Add(new IsInline());
attachments.Add(new Id());


var inReplyTo = new InReplyTo
{
};

var categories = new List<Categories>();
categories.Add([
  "categories-value"
]);

var newParticipants = new List<NewParticipants>();
newParticipants.Add(new EmailAddress());


var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var sender = new Sender
{
	EmailAddress = emailAddress,
};

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var from = new From
{
	EmailAddress = emailAddress,
};

var body = new Body
{
	ContentType = "",
	Content = "content-value",
};

var post = new Post
{
	Body = body,
	ReceivedDateTime = "2016-10-19T10:37:00Z",
	HasAttachments = true,
	From = from,
	Sender = sender,
	ConversationThreadId = "conversationThreadId-value",
	NewParticipants = newParticipants,
	ConversationId = "conversationId-value",
	CreatedDateTime = "2016-10-19T10:37:00Z",
	LastModifiedDateTime = "2016-10-19T10:37:00Z",
	ChangeKey = "changeKey-value",
	Categories = categories,
	Id = "id-value",
	InReplyTo = inReplyTo,
	Attachments = attachments,
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"]
	.reply(post);
	.Request()
	.PostAsync()

```