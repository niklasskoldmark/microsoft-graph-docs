
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var alternativeSecurityIds = new List<AlternativeSecurityIds>();
alternativeSecurityIds.Add(new Type());
alternativeSecurityIds.Add(new Key());


var device = new Device
{
	AccountEnabled = false,
	AlternativeSecurityIds = alternativeSecurityIds,
	DeviceId = "4c299165-6e8f-4b45-a5ba-c5d250a707ff",
	DisplayName = "Test device",
	OperatingSystem = "linux",
	OperatingSystemVersion = "1",
};

await graphClient.Devices
	.Request()
	.AddAsync(device);

```