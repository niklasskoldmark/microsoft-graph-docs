
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var directoryObject = new DirectoryObject
{
};

var registeredUser = new RegisteredUser
{
	DirectoryObject = directoryObject,
};

await graphClient.Devices["{id}"].RegisteredUsers
	.Request()
	.AddAsync(registeredUser);

```