
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var values = new List<Values>();
values.Add(new Name());
values.Add(new Value());


var setting = new Setting
{
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.Settings
	.Request()
	.AddAsync(setting);

```