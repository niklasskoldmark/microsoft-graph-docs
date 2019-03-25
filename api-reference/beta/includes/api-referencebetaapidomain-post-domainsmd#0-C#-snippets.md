
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var domain = new Domain
{
	Id = "contoso.com",
};

await graphClient.Domains
	.Request()
	.AddAsync(domain);

```