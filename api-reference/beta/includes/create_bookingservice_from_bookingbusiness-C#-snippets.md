
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var staffMemberIds = new List<StaffMemberIds>();
staffMemberIds.Add([
  "d90d1e8c-5cfe-48cf-a2d5-966267375b6a",
  "2f5f8794-0b29-45b5-b56a-2eb5ff7aa880"
]);

var schedulingPolicy = new SchedulingPolicy
{
	@odata.type = "#microsoft.graph.bookingSchedulingPolicy",
	AllowStaffSelection = true,
	MaximumAdvance = "P10D",
	MinimumLeadTime = "PT10H",
	SendConfirmationsToOwner = true,
	TimeSlotInterval = "PT1H",
};

var defaultReminders = new List<DefaultReminders>();
defaultReminders.Add(new @odata.type());
defaultReminders.Add(new Message());
defaultReminders.Add(new Offset());
defaultReminders.Add(new Recipients@odata.type());
defaultReminders.Add(new Recipients());


var address = new Address
{
	@odata.type = "#microsoft.graph.physicalAddress",
	City = "Buffalo",
	CountryOrRegion = "USA",
	PostalCode = "98052",
	PostOfficeBox = null,
	State = "NY",
	Street = "4567 First Street",
	Type@odata.type = "#microsoft.graph.physicalAddressType",
	Type = null,
};

var defaultLocation = new DefaultLocation
{
	@odata.type = "#microsoft.graph.location",
	Address = address,
	Coordinates = null,
	DisplayName = "Contoso Lunch Delivery",
	LocationEmailAddress = null,
	LocationType@odata.type = "#microsoft.graph.locationType",
	LocationType = null,
	LocationUri = null,
	UniqueId = null,
	UniqueIdType@odata.type = "#microsoft.graph.locationUniqueIdType",
	UniqueIdType = null,
};

var service = new Service
{
	@odata.type = "#microsoft.graph.bookingService",
	DefaultDuration = "PT1H30M",
	DefaultLocation = defaultLocation,
	DefaultPrice = 10.0,
	DefaultPriceType@odata.type = "#microsoft.graph.bookingPriceType",
	DefaultPriceType = "fixedPrice",
	DefaultReminders@odata.type = "#Collection(microsoft.graph.bookingReminder)",
	DefaultReminders = defaultReminders,
	Description = "Individual bento box lunch delivery",
	DisplayName = "Bento",
	IsHiddenFromCustomers = false,
	Notes = "Home-cooked special",
	PostBuffer = "PT10M",
	PreBuffer = "PT5M",
	SchedulingPolicy = schedulingPolicy,
	StaffMemberIds@odata.type = "#Collection(String)",
	StaffMemberIds = staffMemberIds,
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Services
	.Request()
	.AddAsync(service);

```