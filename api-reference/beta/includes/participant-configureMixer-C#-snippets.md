
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var clientContext = "d45324c1-fcb5-430a-902c-f20af696537c";

var participantMixerLevels = new List<ParticipantMixerLevels>();
participantMixerLevels.Add(new Participant());
participantMixerLevels.Add(new Exclusive());
participantMixerLevels.Add(new Ducking());
participantMixerLevels.Add(new SourceLevels());


await graphClient.App.Calls["{id}"].Participants
	.configureMixer(participantMixerLevels,clientContext);
	.Request()
	.PostAsync()

```