
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var values = new Values
{
};

var icon = new Icon
{
	Set = "set-value",
	Index = 99,
};

var operator = new Operator
{
};

var criteria = new Criteria
{
	Criterion1 = "criterion1-value",
	Criterion2 = "criterion2-value",
	Color = "color-value",
	Operator = operator,
	Icon = icon,
	DynamicCriteria = "dynamicCriteria-value",
	Values = values,
	FilterOn = "filterOn-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns["{id|name}"].Filter
	.apply(criteria);
	.Request()
	.PostAsync()

```