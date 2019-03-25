
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var section = new Section
{
	DisplayName = "Section name",
};

await graphClient.Me.Onenote.SectionGroups["{id}"].Sections
	.Request()
	.AddAsync(section);

```