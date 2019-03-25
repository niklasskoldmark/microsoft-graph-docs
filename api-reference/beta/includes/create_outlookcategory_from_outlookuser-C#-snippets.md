
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var masterCategorie = new MasterCategorie
{
	DisplayName = "Project expenses",
	Color = "preset9",
};

await graphClient.Me.Outlook.MasterCategories
	.Request()
	.AddAsync(masterCategorie);

```