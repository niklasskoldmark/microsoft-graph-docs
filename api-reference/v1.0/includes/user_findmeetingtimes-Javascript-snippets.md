
```Javascript

// Some callback function
const authProvider: AuthProvider = (callback: AuthProviderCallback) => { 
	// Your logic for getting and refreshing accessToken 
	// Error should be passed in case of error while authenticating 
	// accessToken should be passed upon successful authentication 
	callback(error, accessToken);
};

let options: Options = {
		authProvider,
};

const client = Client.init(options);

const findMeetingTimes = {
  attendees: [ 
    { 
      type: "required",  
      emailAddress: { 
        name: "Samantha Booth",
        address: "samanthab@contoso.onmicrosoft.com" 
      } 
    }
  ],  
  locationConstraint: { 
    isRequired: "false",  
    suggestLocation: "false",  
    locations: [ 
      { 
        resolveAvailability: "false",
        displayName: "Conf room Hood" 
      } 
    ] 
  },  
  timeConstraint: {
    activityDomain:"unrestricted", 
    timeslots: [ 
      { 
        start: { 
          dateTime: "2017-04-17T09:00:00",  
          timeZone: "Pacific Standard Time" 
        },  
        end: { 
          dateTime: "2017-04-19T17:00:00",  
          timeZone: "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  meetingDuration: "PT2H",
  returnSuggestionReasons: true,
  minimumAttendeePercentage: 100.0
}
;

client.api('/me/findMeetingTimes').post({findMeetingTimes : findMeetingTimes});

```