
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new DirectoryObject
{
};

var memberO = new MemberO
{
	DirectoryObject = directoryObject,
};

await graphClient.Contacts["{id}"].MemberOf
	.Request()
	.AddAsync(memberO);

```