
```C#

GraphServiceClient graphClient = new GraphServiceClient();

var bargeInAllowed = True;

var clientContext = "d45324c1-fcb5-430a-902c-f20af696537c";

var prompts = new List<Prompts>();
prompts.Add(new @odata.type());
prompts.Add(new MediaInfo());
prompts.Add(new Loop());


var maxRecordDurationInSeconds = 1800;

var initialSilenceTimeoutInSeconds = 10;

var maxSilenceTimeoutInSeconds = 2;

var recordingFormat = "wav";

var playBeep = True;

var streamWhileRecording = True;

var stopTones = new List<StopTones>();
stopTones.Add([
  "#",
  "11",
  "*"
]);

await graphClient.App.Calls["{id}"]
	.record(prompts,bargeInAllowed,initialSilenceTimeoutInSeconds,maxSilenceTimeoutInSeconds,maxRecordDurationInSeconds,playBeep,streamWhileRecording,stopTones,clientContext);
	.Request()
	.PostAsync()

```