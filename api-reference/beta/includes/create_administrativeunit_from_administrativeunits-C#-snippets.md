
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var administrativeUnit = new AdministrativeUnit
{
	DisplayName = "Seattle District Technical Schools",
	Description = "Seattle district technical schools administration",
	Visibility = "true",
};

await graphClient.AdministrativeUnits
	.Request()
	.AddAsync(administrativeUnit);

```