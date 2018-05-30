# Conferences
In order to create a lovely and handcrafted PWA or app on your own for your most beloved conference, it would be nice to get the schedule data in JSON format.

## Contribute
Feel free to send pull requests for your favorite conference.

## Data Structure
The datastructure is pretty straightforward: 

```json
{
    "conference": "The Main of the conference",
    "description": "The conference description",
    "dataversion": "Data version identifier",
    "timezone": "Time/Zone", // e.g. "Europe/Berlin"
    "social": {
        // a map of social accounts/links, e.g.
        // "twitter": "@twitter",
        // "instagram": ...
        "web": "https://conference.example"
    },
    "links": [
        {
            "type": "code-of-conduct",
            "url": "https://conference.example/CoC.html",
            "text": "Code of Conduct"
        },
        {
            "type": "imprint",
            "url": "https://conference.example/imprint.html",
            "text": "Imprint"
        },
        {
            "type": "schedule",
            "url": "https://conference.example/schedule.html",
            "text": "Schedule"
        },
        {
            "type": "website",
            "url": "https://conference.example/",
            "text": "Website"
        }
    ],
    "talks": [
        // talk objects
    ]
}
```

Where a talk object has the following structure:

```json
{
    "track": "the track, stage or room",
    "id": "genuine-id-for-the-talk",
    // datetime: UTC string
    "datetime": "Sat, 02 Jun 2018 06:30:00 GMT",
    "details": {
        "speaker": {
            "fullname": "the name of the speaker",
            "social": {
                // same as social media mapping above
            }
        },
        "title": "the title of the talk",
        "description": [
            'the description of the talk',
            'separated by lines/array items',
            'if you want to',
            '',
            'why the string array?',
            '- you can structure the information',
            '- like bullet points'
        ],
        "links": [
            {
                "url": "https://conference.example/talks/a-talk.html",
                "text": "Talk details",
                "type": "default-link"
            }
        ]
    }
},
```
