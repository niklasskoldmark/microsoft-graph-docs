
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var senderEmailAddress = new SenderEmailAddress
{
	Name = "Samantha Booth",
	Address = "samanthab@adatum.onmicrosoft.com",
};

var override = new Override
{
	ClassifyAs = "focused",
	SenderEmailAddress = senderEmailAddress,
};

await graphClient.Me.InferenceClassification.Overrides
	.Request()
	.AddAsync(override);

```