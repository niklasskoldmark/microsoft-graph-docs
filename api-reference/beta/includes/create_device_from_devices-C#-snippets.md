
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var alternativeSecurityIds = new List<AlternativeSecurityIds>();
alternativeSecurityIds.Add(new Type());
alternativeSecurityIds.Add(new IdentityProvider());
alternativeSecurityIds.Add(new Key());


var device = new Device
{
	AccountEnabled = true,
	AlternativeSecurityIds = alternativeSecurityIds,
	ApproximateLastSignInDateTime = "2016-10-19T10:37:00Z",
	DeviceId = "deviceId-value",
	DeviceMetadata = "deviceMetadata-value",
	DeviceVersion = 99,
};

await graphClient.Devices
	.Request()
	.AddAsync(device);

```