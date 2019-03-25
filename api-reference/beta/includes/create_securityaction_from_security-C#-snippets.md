
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var vendorInformation = new VendorInformation
{
	Provider = "Windows Defender ATP",
	Vendor = "Microsoft",
};

var parameters = new List<Parameters>();
parameters.Add(new Name());
parameters.Add(new Value());


var securityAction = new SecurityAction
{
	Name = "BlockIp",
	ActionReason = "Test",
	Parameters = parameters,
	VendorInformation = vendorInformation,
};

await graphClient.Security.SecurityActions
	.Request()
	.AddAsync(securityAction);

```