
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var attachments = new List<Attachments>();
attachments.Add(new @odata.type());
attachments.Add(new Name());
attachments.Add(new ContentBytes());


var message = new Message
{
	Attachments = attachments,
};

var comment = "Please take a look at the attached guidelines before you decide on the name.";

await graphClient.Me.Messages["AAMkADA1MTAAAH5JaKAAA="]
	.replyAll(message,comment);
	.Request()
	.PostAsync()

```