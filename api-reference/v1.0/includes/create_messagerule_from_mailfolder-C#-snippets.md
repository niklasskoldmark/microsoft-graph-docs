
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var forwardTo = new List<ForwardTo>();
forwardTo.Add(new EmailAddress());


var actions = new Actions
{
	ForwardTo = forwardTo,
	StopProcessingRules = true,
};

var senderContains = new List<SenderContains>();
senderContains.Add([
  "adele"
]);

var conditions = new Conditions
{
	SenderContains = senderContains,
};

var messageRule = new MessageRule
{
	DisplayName = "From partner",
	Sequence = 2,
	IsEnabled = true,
	Conditions = conditions,
	Actions = actions,
};

await graphClient.Me.MailFolders["inbox"].MessageRules
	.Request()
	.AddAsync(messageRule);

```