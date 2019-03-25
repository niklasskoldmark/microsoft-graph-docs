
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var sectionGroup = new SectionGroup
{
	DisplayName = "Section group name",
};

await graphClient.Me.Onenote.SectionGroups["{id}"].SectionGroups
	.Request()
	.AddAsync(sectionGroup);

```