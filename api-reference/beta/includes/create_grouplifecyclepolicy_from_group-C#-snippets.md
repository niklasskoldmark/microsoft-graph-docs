
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var groupLifecyclePolicie = new GroupLifecyclePolicie
{
	GroupLifetimeInDays = 100,
	ManagedGroupTypes = "Selected",
	AlternateNotificationEmails = "admin@contoso.com",
};

await graphClient.GroupLifecyclePolicies
	.Request()
	.AddAsync(groupLifecyclePolicie);

```