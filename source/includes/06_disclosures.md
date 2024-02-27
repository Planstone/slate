# Sessions

## Get All Speakers


```shell
curl "https://apps.planion.com/feed/v1/disclosures?where={"account":"ACCOUNT","conference":"CONTAINER_ID"}" \
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

The disclosures method gives a simplified listing of all disclosure data Planstone has for this event.  This API will disseminate information regardless of its “status” in Planstone.

To use this method, you must utilize the Planstone Disclosure Module.

If you wish to utilize this disclosure API, please talk to your account manager about the use case, and we’ll discuss in more detail how it works.


### HTTP Request

`GET https://apps.planion.com/feed/v1/disclosures?where={"account":"ACCOUNT","conference":"CONTAINER_ID"}`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
account | true | Your account acronym
conference | true | the conference container ID.  Provided by Planstone or your Planstone Contact.

<aside class="success">
Remember — All API Endpoints are Paginated.  Use the data links to find the first, next, and last pages of data!
</aside>