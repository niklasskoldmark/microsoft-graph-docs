
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var privilegedRoleAssignment = new PrivilegedRoleAssignment
{
	UserId = "userId-value",
	RoleId = "roleId-value",
};

await graphClient.PrivilegedRoleAssignments
	.Request()
	.AddAsync(privilegedRoleAssignment);

```