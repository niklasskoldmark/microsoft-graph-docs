
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var phones = new List<Phones>();
phones.Add(new Number());
phones.Add(new Type());


var emailAddresses = new List<EmailAddresses>();
emailAddresses.Add(new Address());
emailAddresses.Add(new Name());
emailAddresses.Add(new Type());
emailAddresses.Add(new Address());
emailAddresses.Add(new Name());
emailAddresses.Add(new Type());
emailAddresses.Add(new OtherLabel());


var contact = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	Phones = phones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contact);

```