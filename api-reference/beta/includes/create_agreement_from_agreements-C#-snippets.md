
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var files = new List<Files>();
files.Add(new FileName());
files.Add(new Language());
files.Add(new IsDefault());
files.Add(new FileData());


var agreement = new Agreement
{
	DisplayName = "MSGraph Sample",
	IsViewingBeforeAcceptanceRequired = true,
	Files = files,
};

await graphClient.Agreements
	.Request()
	.AddAsync(agreement);

```