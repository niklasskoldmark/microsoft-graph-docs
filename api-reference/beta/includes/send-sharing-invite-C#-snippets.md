
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var recipients = new List<Recipients>();
recipients.Add(new Email());


var message = "Here's the file that we're collaborating on.";

var requireSignIn = True;

var sendInvitation = True;

var roles = new List<Roles>();
roles.Add([
  "write"
]);

var password = "password123";

var expirationDateTime = 7/15/2018 2:00:00 PM;

await graphClient.Me.Drive.Items["{item-id}"]
	.invite(requireSignIn,roles,sendInvitation,message,recipients,expirationDateTime,password);
	.Request()
	.PostAsync()

```