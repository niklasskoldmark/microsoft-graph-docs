
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryRole = new DirectoryRole
{
	RoleTemplateId = "roleTemplateId-value",
};

await graphClient.DirectoryRoles
	.Request()
	.AddAsync(directoryRole);

```