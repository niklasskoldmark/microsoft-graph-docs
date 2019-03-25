
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var addLicenses = new List<AddLicenses>();
addLicenses.Add(new DisabledPlans());
addLicenses.Add(new SkuId());
addLicenses.Add(new DisabledPlans());
addLicenses.Add(new SkuId());


var removeLicenses = new List<RemoveLicenses>();
removeLicenses.Add([]);

await graphClient.Me
	.assignLicense(addLicenses,removeLicenses);
	.Request()
	.PostAsync()

```