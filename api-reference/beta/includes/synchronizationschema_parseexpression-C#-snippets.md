
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var expression = "Replace([preferredLanguage], "-", , , "_", ,  )";

var targetAttributeDefinition = ;

var properties = new List<Properties>();
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value());
properties.Add(new Key());
properties.Add(new Value@odata.type());
properties.Add(new Value());


var testInputObject = new TestInputObject
{
	Definition = null,
	Properties = properties,
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{id}"].Schema
	.parseExpression(expression,testInputObject,targetAttributeDefinition);
	.Request()
	.PostAsync()

```