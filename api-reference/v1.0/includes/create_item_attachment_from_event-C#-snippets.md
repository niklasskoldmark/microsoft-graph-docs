
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var end = new End
{
	DateTime = "2016-12-02T19:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new Start
{
	DateTime = "2016-12-02T18:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new Body
{
	ContentType = "HTML",
	Content = "Let's look for funding!",
};

var item = new Item
{
	@odata.type = "microsoft.graph.event",
	Subject = "Discuss gifts for children",
	Body = body,
	Start = start,
	End = end,
};

var attachment = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "Holiday event",
	Item = item,
};

await graphClient.Me.Events["AAMkAGI1AAAt9AHjAAA="].Attachments
	.Request()
	.AddAsync(attachment);

```