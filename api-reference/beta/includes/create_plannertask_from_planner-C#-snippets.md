
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var fbab97d0-4932-4511-b675-204639209557 = new Fbab97d0-4932-4511-b675-204639209557
{
	@odata.type = "#microsoft.graph.plannerAssignment",
	OrderHint = " !",
};

var assignments = new Assignments
{
	Fbab97d0-4932-4511-b675-204639209557 = fbab97d0-4932-4511-b675-204639209557,
};

var task = new Task
{
	PlanId = "xqQg5FS2LkCp935s-FIFm2QAFkHM",
	BucketId = "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
	Title = "Update client list",
	Assignments = assignments,
};

await graphClient.Planner.Tasks
	.Request()
	.AddAsync(task);

```