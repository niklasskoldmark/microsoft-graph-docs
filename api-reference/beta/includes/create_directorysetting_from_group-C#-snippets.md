
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var values = new List<Values>();
values.Add(new Name());
values.Add(new Value());


var directorySetting = new DirectorySetting
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

var setting = new Setting
{
	DirectorySetting = directorySetting,
};

await graphClient.Groups["{id}"].Settings
	.Request()
	.AddAsync(setting);

```