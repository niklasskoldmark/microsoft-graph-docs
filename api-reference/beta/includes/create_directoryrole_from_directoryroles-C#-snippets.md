
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryRole = new DirectoryRole
{
	Description = "description-value",
	DisplayName = "displayName-value",
	RoleTemplateId = "roleTemplateId-value",
};

await graphClient.DirectoryRoles
	.Request()
	.AddAsync(directoryRole);

```