
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var plan = new Plan
{
	Owner = "ebf3b108-5234-4e22-b93d-656d7dae5874",
	Title = "title-value",
};

await graphClient.Planner.Plans
	.Request()
	.AddAsync(plan);

```