
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<Value>();
value.Add(new ActivityGroupNames());
value.Add(new Confidence());
value.Add(new Description());
value.Add(new ExpirationDateTime());
value.Add(new ExternalId());
value.Add(new FileHashType());
value.Add(new FileHashValue());
value.Add(new KillChain());
value.Add(new MalwareFamilyNames());
value.Add(new Severity());
value.Add(new Tags());
value.Add(new TargetProduct());
value.Add(new ThreatType());
value.Add(new TlpLevel());
value.Add(new ActivityGroupNames());
value.Add(new Confidence());
value.Add(new Description());
value.Add(new ExpirationDateTime());
value.Add(new ExternalId());
value.Add(new FileHashType());
value.Add(new FileHashValue());
value.Add(new KillChain());
value.Add(new MalwareFamilyNames());
value.Add(new Severity());
value.Add(new Tags());
value.Add(new TargetProduct());
value.Add(new ThreatType());
value.Add(new TlpLevel());


await graphClient.Security.TiIndicators
	.submitTiIndicators(value);
	.Request()
	.PostAsync()

```