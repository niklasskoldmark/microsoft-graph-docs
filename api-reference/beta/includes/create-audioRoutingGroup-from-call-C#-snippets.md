
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var receivers = new List<Receivers>();
receivers.Add([
  "550fae72-d251-43ec-868c-373732c2704f"
]);

var sources = new List<Sources>();
sources.Add([
  "632899f8-2ea1-4604-8413-27bd2892079f"
]);

var audioRoutingGroup = new AudioRoutingGroup
{
	Id = "oneToOne",
	RoutingMode = "oneToOne",
	Sources = sources,
	Receivers = receivers,
};

await graphClient.App.Calls["{id}"].AudioRoutingGroups
	.Request()
	.AddAsync(audioRoutingGroup);

```