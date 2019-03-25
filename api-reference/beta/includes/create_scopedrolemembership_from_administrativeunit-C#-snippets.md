
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var roleMemberInfo = new RoleMemberInfo
{
	Id = "id-value",
};

var scopedRoleMember = new ScopedRoleMember
{
	RoleId = "roleId-value",
	RoleMemberInfo = roleMemberInfo,
};

await graphClient.AdministrativeUnits["{id}"].ScopedRoleMembers
	.Request()
	.AddAsync(scopedRoleMember);

```