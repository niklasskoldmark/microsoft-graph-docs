
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var privilegedApprova = new PrivilegedApprova
{
	UserId = "userId-value",
	RoleId = "roleId-value",
	ApprovalType = "approvalType-value",
	ApprovalState = "approvalState-value",
	ApprovalDuration = "datetime-value",
};

await graphClient.PrivilegedApproval
	.Request()
	.AddAsync(privilegedApprova);

```