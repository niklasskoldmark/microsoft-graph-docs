
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var values = new List<Values>();
values.Add(new Name());
values.Add(new Value());


var groupSetting = new GroupSetting
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.GroupSettings
	.Request()
	.AddAsync(groupSetting);

```