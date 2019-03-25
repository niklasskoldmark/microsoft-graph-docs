
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var clientContext = "d45324c1-fcb5-430a-902c-f20af696537c";

var prompts = new List<Prompts>();
prompts.Add(new @odata.type());
prompts.Add(new MediaInfo());
prompts.Add(new Loop());


await graphClient.App.Calls["{id}"]
	.playPrompt(prompts,clientContext);
	.Request()
	.PostAsync()

```