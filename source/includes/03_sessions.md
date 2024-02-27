# Sessions

## Get All Sessions


```shell
curl "https://apps.planion.com/feed/v1/sessions?where={"account":"ACCOUNT","conference":"CONTAINER_ID"}" \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
   "_items": [
       {
           "custom13name": null,
           "endDate": "",
           "credits8": "0.0",
           "credits9": "0.0",
           "location": "",
           "custom10name": null,
           "credits2": "0.0",
           "credits3": "0.0",
           "credits1": "0.0",
           "credits6": "0.0",
           "credits7": "0.0",
           "credits4": "0.0",
           "credits5": "0.0",
           "SessionDetailsURL": "http://www.planion.com/Web.User/SesDet?ACCOUNT=myaccount&CONF=2018&SCHEDID=212899",
           "custom20name": null,
           "schedid": "21899",
           "custom14name": null,
           "endTime": " ",
           "credits9_label": "",
           "custom18name": null,
           "custom3name": "Custom Eval question 1",
           "custom5name": "Custom Eval question 2",
           "credits6_label": "",
           "custom9name": "Credit Units",
           "credits8_label": "",
           "conference": "2018",
           "roomname": "Ballroom A",
           "tracks": [],
           "sesid": "12147",
           "_created": "Thu, 01 Jan 1970 00:00:00 GMT",
           "credits3_label": "",
           "custom12": null,
           "custom19name": null,
           "custom16name": null,
           "custom20": null,
           "learning_objective9": "",
           "learning_objective8": "",
           "sessionName": "Test 2",
           "published": true,
           "learning_objective1": "",
           "learning_objective3": "",
           "learning_objective2": "",
           "learning_objective5": "",
           "learning_objective4": "",
           "learning_objective7": "",
           "learning_objective6": "",
           "startDate": "",
           "mobileActionURL": "url for your mobile company",
           "credits1_label": "",
           "custom16": null,
           "custom17": null,
           "custom14": null,
           "custom15": null,
           "credits7_label": "",
           "custom13": null,
           "custom10": null,
           "custom11": null,
           "custom18": null,
           "custom19": null,
           "_links": {
               "self": {
                   "href": "sessions/5aaa7a013d0b7f000b72492b",
                   "title": "session"
               }
           },
           "custom11name": null,
           "credits4_label": "",
           "custom17name": null,
           "account": "myaccount",
           "custom6name": "Custom Eval comment 2",
           "sessionType": "General Session",
           "custom12name": null,
           "_etag": "f0a6b49bdb35e2194fd557e65dbe90646af5cc27",
           "credits5_label": "",
           "custom8": null,
           "custom9": null,
           "custom4": null,
           "custom5": null,
           "custom6": null,
           "custom7": null,
           "custom1": null,
           "custom2": null,
           "custom3": null,
           "custom4name": null,
           "custom15name": null,
           "adanotes": null,
           "custom8name": "Custom Eval comment 3",
           "speakers": [
               {
                   "cargo": "",
                   "description": null,
                   "title": "",
                   "pid": "65076",
                   "pslinkid": "38028",
                   "role": "Eval Contact",
                   "sortorder": "500",
                   "startTime": " ",
                   "published": null,
                   "endTime": " ",
                   "resources": [],
                   "affil": ""
               },
               {
                   "cargo": "",
                   "description": null,
                   "title": "",
                   "pid": "10024",
                   "pslinkid": "38029",
                   "role": "Declined Session Moderator",
                   "sortorder": "002",
                   "startTime": " ",
                   "published": true,
                   "endTime": " ",
                   "resources": [],
                   "affil": ""
               },
               {
                   "cargo": "",
                   "description": null,
                   "title": "",
                   "pid": "10006",
                   "pslinkid": "38030",
                   "role": "Declined Session Presenter",
                   "sortorder": "001",
                   "startTime": " ",
                   "published": true,
                   "endTime": " ",
                   "resources": [],
                   "affil": ""
               },
               {
                   "cargo": "",
                   "description": null,
                   "title": "",
                   "pid": "65294",
                   "pslinkid": "38031",
                   "role": "Declined Session Organizer",
                   "sortorder": "003",
                   "startTime": " ",
                   "published": true,
                   "endTime": " ",
                   "resources": [],
                   "affil": ""
               },
               {
                   "cargo": "",
                   "description": null,
                   "title": "",
                   "pid": "46549",
                   "pslinkid": "38305",
                   "role": "Eval Contact",
                   "sortorder": "300",
                   "startTime": " ",
                   "published": null,
                   "endTime": " ",
                   "resources": [],
                   "affil": ""
               }
           ],
           "learning_objective10": "",
           "custom2name": "Track Sponsor",
           "description": "Some long session description that may contain html code",
           "custom1name": "2-Part Session",
           "startTime": " ",
           "credits2_label": "",
           "custom7name": "Custom Eval question 3",
           "_updated": "Thu, 01 Jan 1970 00:00:00 GMT",
           "sessionClientID": "C101",
           "_id": "5aaa7a013d0b7f000b72492b",
           "ticketed": null
       }
   ]
}

```

This endpoint retrieves all sessions.

The sessions endpoint will publish a complete listing of Planstone's sessions for your event.  This includes sessions, and speakers indicated as “published” in the system.  Your other vendors and systems may have a business need to know about data that attendees may not, like committees or unpublished people for sessions like a moderator or evaluation contact.

The Speakers array within each session provides the details regarding each speaking engagement.  This shows whether or not this person for this engagement should be published.  This is important to tell your other vendors about.

To get a speaker's information, cross reference their object from the Speakers method, linking based on PID  ( Person - ID ), which is unique per person.

SCHEDID is the best Unique Identifier from Planstone.

SessionClientID is the identifier our mutual client assigns, which may not be unique or have a value.


### HTTP Request

`GET https://apps.planion.com/feed/v1/sessions?where={"account":"ACCOUNT","conference":"CONTAINER_ID"}`


Get a second page of data:

`GET https://apps.planion.com/feed/v1/sessions?where={"account":"ACCOUNT","conference":"CONTAINER_ID"}&page=2`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
account | true | Your account acronym
conference | true | the conference container ID.  Provided by Planstone or your Planstone Contact.
page | false | request a given page of data

<aside class="success">
Remember — All API Endpoints are Paginated.  Use the data links to find the first, next, and last pages of data!
</aside>


### Data Response Elements

Key | Sample Value | Description 
----|--------------| ----------
_id | 65dd3f260b568d8c255fd53b  | Internal ID of the API. API consumers should not use this
account  | AAA | Your Account Acronym                                                        
conference | AM2024 | conference_acronym          
session_updated_at               | 2024-01-31 15:30:43 | updated at timestamp of the session 
schedule_updated_at              | 2023-12-19 13:41:10  | updated at timestamp of schedule 
updated_at                       | 2024-01-31 15:30:43  | internal API field, please ignore this field 
clientid                         | 101a | The friendly ID assigned to a session by the client 
sessionClientID                  | 101a | The friendly ID assigned to a session by the client (same as field above)
sessionName                      | Novelty of Ice Cream | The Session Title 
description                      | Talk to researchers about their work at this in-person poster session! Sunday, Monday, and Tuesday each feature different posters, so come back each day. | description of the session.  May contain HTML markup
custom1name                      | sampleCustom1Name | Custome Field One Name or Label                                                                                             
custom2name                      | sampleCustom2Name | Custom Two Field Name or Label                                                                                               
custom3name                      | sampleCustom3Name | Custom Three Field Name or Label                                                                                                 
custom4name                      | sampleCustom4Name | CustomFour Field Name or Label                                                                                      
custom5name | sampleCustom5Name | CustomFive Field Name or Label
custom6name | sampleCustom6Name | CustomSix Field Name or Label
custom7name | sampleCustom7Name | CustomSeven Field Name or Label
custom8name | sampleCustom8Name | CustomEight Field Name or Label
custom9name | sampleCustom9Name | CustomNine Field Name or Label
custom10name | sampleCustom10Name | Custom Ten Field Name or Label
custom11name | sampleCustom11Name | CustomEleven Field Name or Label
custom12name | sampleCustom12Name | CustomTwelve Field Name or Label
custom13name | sampleCustom13Name | CustomThirteen Field Name or Label
custom14name | sampleCustom14Name | CustomFourteen Field Name or Label
custom15name | sampleCustom15Name | CustomFifteen Field Name or Label
custom16name | sampleCustom16Name | CustomSixteen Field or label
custom17name | sampleCustom17Name | CustomSeventeen Field or label
custom18name | sampleCustom18Name | CustomEighteen Field or label
custom19name | sampleCustom19Name | CustomSeventeen Field or Label
custom20name | sampleCustom20Name | CustomSeventeen Field or or Label                                                                                              
learning_objective1 | Learning Objective 1 | Learning Object 1
learning_objective2 | Learning Objective 2 | Learning Objective 2
learning_objective3 | Learning Objective 3 | learning Objective 3
learning_objective4 | Learning Objective 4 | learning Objective 4
learning_objective5 | Learning Objective 5 | learning Objective 5
learning_objective6 | Learning Objective 6 | Learning Objective 6
learning_objective7 | Learning Objective 7 | Learning Objective 7
learning_objective8 | Learning Objective 8 | Learning Objective 8
learning_objective9 | Learning Objective 9 | Learning Objective 9
learning_objective10 | Learning Objective 10 | Learning Objective 10                                                                                                             
credits1                         | 0.0 | credit value assigned to this credit bucket                                                                                                         
credits1_label                   | CME_Physicians | the label assigned to this credit bucket                                                                                             
sched_roomname                   | Henry B. Gonzalez Convention Center: Exhibit Hall 4 | The scheduled room name                                                   
roomid                           | 910024 | The Room ID assigned to the Session, only used if the Scheduling module                                                                                                      
roomname                         | Exhibit Hall 4                                                                                              
hotelname                        | Henry B. Gonzalez Convention Center                                                                         
startDate                        | 2024-11-03                                                                                                  
startTime                        | 07:30 pm                                                                                                    
rstartmins                       | 1170                                                                                                        
endTime                          | 08:30 pm                                                                                                    
rendmins                         | 1230                                                                                                        
sesid                            | 910153                                                                                                      
published                        | 1                                                                                                           
schedid                          | 910152                                                                                                      
sestype                          | 101136                                                                                                      
sessionType                      | Special Event                                                                                               
SessionDetailsURL                | [Session Details](https://TOS.planion.com/Web.User/SesDet?ACCOUNT=TOS&CONF=OW2024&SCHEDID=910152&ssoOverride=OFF) 
planstoneDesktopUserActionURL    | [Desktop User Action](https://TOS.planion.com/Z?HH0Z06796&schedid=910152)                                    
has_handouts                     | false | a boolean flag indicating if the session has handouts or not                                                                                                      
_meta.page                       | 2  | the current page of data                                                                                                          
_meta.max_results                | 100 | Max results per page                                                                                                         
_meta.total                      | 823 | Total number of Session objects in Total                                                                                                          
