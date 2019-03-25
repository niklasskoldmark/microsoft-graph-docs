
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var members@odata.bind = new List<Members@odata.bind>();
members@odata.bind.Add([
  "https://graph.microsoft.com/beta/users/ff7cb387-6688-423c-8188-3da9532a73cc",
  "https://graph.microsoft.com/beta/users/69456242-0067-49d3-ba96-9de6f2728e14"
]);

var owners@odata.bind = new List<Owners@odata.bind>();
owners@odata.bind.Add([
  "https://graph.microsoft.com/beta/users/26be1845-4119-4801-a799-aea79d09f1a2"
]);

var groupTypes = new List<GroupTypes>();
groupTypes.Add([
  "Unified"
]);

var group = new Group
{
	Description = "Group with designated owner and members",
	DisplayName = "Operations group",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "operations2019",
	SecurityEnabled = false,
	Owners@odata.bind = owners@odata.bind,
	Members@odata.bind = members@odata.bind,
};

await graphClient.Groups
	.Request()
	.AddAsync(group);

```