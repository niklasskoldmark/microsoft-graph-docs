
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var targets = new List<Targets>();
targets.Add(new EndpointType());
targets.Add(new Identity());
targets.Add(new LanguageId());
targets.Add(new Region());


var targetDisposition = "default";

var timeout = 99;

var maskCallee = False;

var maskCaller = False;

await graphClient.App.Calls["{id}"]
	.redirect(targets,targetDisposition,timeout,maskCallee,maskCaller);
	.Request()
	.PostAsync()

```