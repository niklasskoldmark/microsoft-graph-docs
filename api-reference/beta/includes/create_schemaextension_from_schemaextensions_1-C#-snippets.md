
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var properties = new List<Properties>();
properties.Add(new Name());
properties.Add(new Type());
properties.Add(new Name());
properties.Add(new Type());
properties.Add(new Name());
properties.Add(new Type());


var targetTypes = new List<TargetTypes>();
targetTypes.Add([
  "Group"
]);

var schemaExtension = new SchemaExtension
{
	Id = "graphlearn_courses",
	Description = "Graph Learn training courses extensions",
	TargetTypes = targetTypes,
	Properties = properties,
};

await graphClient.SchemaExtensions
	.Request()
	.AddAsync(schemaExtension);

```