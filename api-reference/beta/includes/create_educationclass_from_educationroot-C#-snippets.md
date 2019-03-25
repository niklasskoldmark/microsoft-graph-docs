
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var classe = new Classe
{
	Description = "Health Level 1",
	ClassCode = "Health 501",
	DisplayName = "Health 1",
	ExternalId = "11019",
	ExternalName = "Health Level 1",
	ExternalSource = "sis",
	MailNickname = "fineartschool.net",
};

await graphClient.Education.Classes
	.Request()
	.AddAsync(classe);

```