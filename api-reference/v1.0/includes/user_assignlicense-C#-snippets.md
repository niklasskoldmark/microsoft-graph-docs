
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var addLicenses = new List<AddLicenses>();
addLicenses.Add(new DisabledPlans());
addLicenses.Add(new SkuId());


var removeLicenses = new List<RemoveLicenses>();
removeLicenses.Add([
  "bea13e0c-3828-4daa-a392-28af7ff61a0f"
]);

await graphClient.Me
	.assignLicense(addLicenses,removeLicenses);
	.Request()
	.PostAsync()

```