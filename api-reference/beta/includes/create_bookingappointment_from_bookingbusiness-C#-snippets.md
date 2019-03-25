
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var start = new Start
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:00:00+03:00",
	TimeZone = "UTC",
};

var address = new Address
{
	@odata.type = "#microsoft.graph.physicalAddress",
	City = "Buffalo",
	CountryOrRegion = "USA",
	PostalCode = "98052",
	PostOfficeBox = null,
	State = "NY",
	Street = "123 First Avenue",
	Type@odata.type = "#microsoft.graph.physicalAddressType",
	Type = null,
};

var serviceLocation = new ServiceLocation
{
	@odata.type = "#microsoft.graph.location",
	Address = address,
	Coordinates = null,
	DisplayName = "Customer location",
	LocationEmailAddress = null,
	LocationType@odata.type = "#microsoft.graph.locationType",
	LocationType = null,
	LocationUri = null,
	UniqueId = null,
	UniqueIdType@odata.type = "#microsoft.graph.locationUniqueIdType",
	UniqueIdType = null,
};

var reminders = new List<Reminders>();
reminders.Add(new @odata.type());
reminders.Add(new Message());
reminders.Add(new Offset());
reminders.Add(new Recipients@odata.type());
reminders.Add(new Recipients());
reminders.Add(new @odata.type());
reminders.Add(new Message());
reminders.Add(new Offset());
reminders.Add(new Recipients@odata.type());
reminders.Add(new Recipients());
reminders.Add(new @odata.type());
reminders.Add(new Message());
reminders.Add(new Offset());
reminders.Add(new Recipients@odata.type());
reminders.Add(new Recipients());


var invoiceDate = new InvoiceDate
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:30:00+03:00",
	TimeZone = "UTC",
};

var end = new End
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-01T15:30:00+03:00",
	TimeZone = "UTC",
};

var address = new Address
{
	@odata.type = "#microsoft.graph.physicalAddress",
	City = "Buffalo",
	CountryOrRegion = "USA",
	PostalCode = "98052",
	PostOfficeBox = null,
	State = "NY",
	Street = "123 First Avenue",
	Type@odata.type = "#microsoft.graph.physicalAddressType",
	Type = null,
};

var customerLocation = new CustomerLocation
{
	@odata.type = "#microsoft.graph.location",
	Address = address,
	Coordinates = null,
	DisplayName = "Customer",
	LocationEmailAddress = null,
	LocationType@odata.type = "#microsoft.graph.locationType",
	LocationType = null,
	LocationUri = null,
	UniqueId = null,
	UniqueIdType@odata.type = "#microsoft.graph.locationUniqueIdType",
	UniqueIdType = null,
};

var appointment = new Appointment
{
	@odata.type = "#microsoft.graph.bookingAppointment",
	CustomerEmailAddress = "jordanm@contoso.com",
	CustomerLocation = customerLocation,
	CustomerName = "Jordan Miller",
	CustomerNotes = "Please be on time.",
	CustomerPhone = "213-555-0199",
	End = end,
	InvoiceAmount = 10.0,
	InvoiceDate = invoiceDate,
	InvoiceId = "1001",
	InvoiceStatus@odata.type = "#microsoft.graph.bookingInvoiceStatus",
	InvoiceStatus = "open",
	InvoiceUrl = "theInvoiceUrl",
	OptOutOfCustomerEmail = false,
	PostBuffer = "PT10M",
	PreBuffer = "PT5M",
	Price = 10.0,
	PriceType@odata.type = "#microsoft.graph.bookingPriceType",
	PriceType = "fixedPrice",
	Reminders@odata.type = "#Collection(microsoft.graph.bookingReminder)",
	Reminders = reminders,
	ServiceId = "57da6774-a087-4d69-b0e6-6fb82c339976",
	ServiceLocation = serviceLocation,
	ServiceName = "Catered bento",
	ServiceNotes = "Customer requires punctual service.",
	Start = start,
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Appointments
	.Request()
	.AddAsync(appointment);

```