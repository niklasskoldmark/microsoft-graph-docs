
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var workingHours = new List<WorkingHours>();
workingHours.Add(new @odata.type());
workingHours.Add(new Day@odata.type());
workingHours.Add(new Day());
workingHours.Add(new TimeSlots@odata.type());
workingHours.Add(new TimeSlots());
workingHours.Add(new @odata.type());
workingHours.Add(new Day@odata.type());
workingHours.Add(new Day());
workingHours.Add(new TimeSlots@odata.type());
workingHours.Add(new TimeSlots());
workingHours.Add(new @odata.type());
workingHours.Add(new Day@odata.type());
workingHours.Add(new Day());
workingHours.Add(new TimeSlots@odata.type());
workingHours.Add(new TimeSlots());
workingHours.Add(new @odata.type());
workingHours.Add(new Day@odata.type());
workingHours.Add(new Day());
workingHours.Add(new TimeSlots@odata.type());
workingHours.Add(new TimeSlots());
workingHours.Add(new @odata.type());
workingHours.Add(new Day@odata.type());
workingHours.Add(new Day());
workingHours.Add(new TimeSlots@odata.type());
workingHours.Add(new TimeSlots());


var staffMember = new StaffMember
{
	@odata.type = "#microsoft.graph.bookingStaffMember",
	ColorIndex = 1,
	DisplayName = "Dana Swope",
	EmailAddress = "danas@contoso.com",
	Role@odata.type = "#microsoft.graph.bookingStaffRole",
	Role = "externalGuest",
	UseBusinessHours = true,
	WorkingHours@odata.type = "#Collection(microsoft.graph.bookingWorkHours)",
	WorkingHours = workingHours,
};

await graphClient.BookingBusinesses["{id}"].StaffMembers
	.Request()
	.AddAsync(staffMember);

```