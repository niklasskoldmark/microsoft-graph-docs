
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var item = new Item
{
};

var attachment = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "name-value",
	Item = item,
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"].Attachments
	.Request()
	.AddAsync(attachment);

```