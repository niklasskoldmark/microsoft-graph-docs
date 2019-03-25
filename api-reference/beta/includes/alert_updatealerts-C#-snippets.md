
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var value = new List<Value>();
value.Add(new AssignedTo());
value.Add(new ClosedDateTime());
value.Add(new Comments());
value.Add(new Feedback());
value.Add(new Id());
value.Add(new Status());
value.Add(new Tags());
value.Add(new VendorInformation());


await graphClient.Security.Alerts
	.updateAlerts(value);
	.Request()
	.PostAsync()

```