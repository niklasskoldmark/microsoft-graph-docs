
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var residenceAddress = new ResidenceAddress
{
	City = "Los Angeles",
	CountryOrRegion = "United States",
	PostalCode = "98055",
	State = "CA",
	Street = "12345 Main St.",
};

var mailingAddress = new MailingAddress
{
	City = "Los Angeles",
	CountryOrRegion = "United States",
	PostalCode = "98055",
	State = "CA",
	Street = "12345 Main St.",
};

var user = new User
{
	DisplayName = "Susana Rocha",
	Id = "14012",
};

var createdBy = new CreatedBy
{
	User = user,
};

var user = new User
{
	DisplayName = "Dion Matheson",
	GivenName = "Dion",
	MiddleName = null,
	Surname = "Matheson",
	Mail = "DionM@contoso.com",
	MobilePhone = "+1 (253) 555-0101",
	CreatedBy = createdBy,
	ExternalSource = "sis",
	MailingAddress = mailingAddress,
	PrimaryRole = "student",
	ResidenceAddress = residenceAddress,
};

await graphClient.Education.Users
	.Request()
	.AddAsync(user);

```