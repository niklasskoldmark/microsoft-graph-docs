
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var businessPhones = new List<BusinessPhones>();
businessPhones.Add([
  "+1 732 555 0102"
]);

var emailAddresses = new List<EmailAddresses>();
emailAddresses.Add(new Address());
emailAddresses.Add(new Name());


var contact = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	BusinessPhones = businessPhones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contact);

```