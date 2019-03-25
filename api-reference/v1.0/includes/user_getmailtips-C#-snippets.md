
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var EmailAddresses = new List<EmailAddresses>();
EmailAddresses.Add([
  "danas@contoso.onmicrosoft.com",
  "fannyd@contoso.onmicrosoft.com"
]);

var MailTipsOptions = "automaticReplies, mailboxFullStatus";

await graphClient.Me
	.getMailTips(emailAddresses,mailTipsOptions);
	.Request()
	.PostAsync()

```