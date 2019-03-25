
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var extensions = new List<Extensions>();
extensions.Add(new @odata.type());
extensions.Add(new ExtensionName());
extensions.Add(new CompanyName());
extensions.Add(new ExpirationDate());
extensions.Add(new TopPicks());


var body = new Body
{
	ContentType = "html",
	Content = "<html><body><div><div><div><div>When and where? </div></div></div></div></body></html>",
};

var post = new Post
{
	Body = body,
	Extensions = extensions,
};

await graphClient.Groups["37df2ff0-0de0-4c33-8aee-75289364aef6"].Threads["AAQkADJizZJpEWwqDHsEpV_KA=="].Posts["AAMkADJiUg96QZUkA-ICwMubAAC1heiSAAA="]
	.reply(post);
	.Request()
	.PostAsync()

```