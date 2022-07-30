## Danish calendar for the years 2000 - 2100 (inclusive)

The calendar itself is in Danish as seen by the below categories:

#### Helligdag
- Nytårsdag
- Palmesøndag
- Skærtorsdag
- Langfredag
- Påskedag
- 2\. påskedag
- Store bededag
- Kristi himmelfartsdag
- Pinsedag
- 2\. pinsedag
- Juledag
- 2\. juledag

#### Kristen mærkedag
- Hellig 3 konger
- Kyndelmisse
- Fastelavn
- Sankthansdag
- Halloween
- Allehelgensdag
- 1., 2., 3. & 4. søndag i advent
- Luciadag
- Juleaften

#### International mærkedag
- Databeskyttelsesdagen
- Kvindernes internationale kampdag
- Arbejdernes internationale kampdag
- FN-dag

#### National mærkedag
- Grundlovsdag
- Valdemarsdag
- Danmarks udsendte

#### Historisk begivenhed
- Stormen på København 1659
- Slaget på Reden 1801
- Bornholm's befrielse 1946
- Besættelsesdagen 1940
- Slaget ved Dybbøl 1864
- Danmarks befrielsesaften 1945
- Danmarks befrielse 1945
- Genforeningen Nordslesvig 1920
- 1\. verdenskrig start 1914
- 1\. verdenskrig slut 1918

#### Traditionel
- Valentinsdag
- Skuddag
- Aprilsnar
- Mors dag
- Fandens fødselsdag
- Sankthansaften
- Allehelgensaften
- Mortensaften
- Mortensdag
- Lille juleaften
- Nytårsaften

#### Årstid
- Jævndøgn
- Solhverv
- Sommertid start
- Sommertid slut
- Lyse nætter start
- Lyse nætter slut

#### Uncategorized / No category
- Sirenetest
- Banklukkedag

This calendar does **not** include the birthdays of royalty.

Descriptions are not included. Feel free to do a search on the internet using the name of a day to find out what it's all about (-;

<BR />


### © Copyright

This project is under normal [copyright](https://en.wikipedia.org/wiki/Copyright). No permissive licenses are granted.

You can download the calender for personal use, but do *not* distribute it. That includes distributing modified versions, derivatives and/or adaptations.

<BR />


### Colours

I've picked these colours for my own caldendar:

| Category                     | Colour             | Hex           | RGB                |
| :--------------------------- | :----------------- | :------------ | :----------------- |
| Helligdag                    | Red                | #FF0000       | rgb(255,   0,   0) |
| Kristen mærkedag             | Purple'ish         | #AC2066&nbsp; | rgb(172,  32, 102) |
| International mærkedag&nbsp; | Blue               | #0000FF       | rgb(  0,   0, 255) |
| National mærkedag            | Lighter blue&nbsp; | #0273FD       | rgb(  2, 115, 253) |
| Historisk begivenhed         | Gray               | #808080       | rgb(128, 128, 128) |
| Traditionel                  | Orange'ish         | #FF8000       | rgb(255, 128,   0) |
| Årstid                       | Green'ish          | #00A200       | rgb(  0, 162,   0) |

<BR />


### Format

The `.ics` is an [iCalendar](https://en.wikipedia.org/wiki/ICalendar) which

> is used and supported by many products, including Google Calendar, Apple Calendar (formerly iCal), HCL Domino (formerly IBM Notes and Lotus Notes), Yahoo! Calendar, Evolution (software), eM Client, Lightning extension for Mozilla Thunderbird and SeaMonkey, and partially by Microsoft Outlook and Novell GroupWise.

<BR />


### Validation

The calendar has been validated without errors at [iCalendar Validator](https://icalendar.org/validator.html). Note that the empty lines in the file results in warnings (`X` represents an line integer):

```
Blank line detected, specification does not address the use of blank lines near line # X
```

The empty lines are kept in the file for the sake of maintainability.

<BR />


### UID

Individual UIDs are unique within the file. They are based on **one** GUID: `4fa00000-8512-4acf-8284-17d99c0f12ae`.

To ensure uniqueness with other calendars `@GraysColour` is appended to all UIDs as specfied in [RFC-5545 iCalendar. Section 3.8.4.7. Unique Identifier](https://icalendar.org/iCalendar-RFC-5545/3-8-4-7-unique-identifier.html).

<BR />


### Why is this not at [Thunderbird Holiday Calendars](https://www.thunderbird.net/en-US/calendar/holidays/)?

This particular Danish calendar is not limited to holidays. There's no reason to add it if most of the content will be removed, see [thunderbird-website issue #239](https://github.com/thundernest/thunderbird-website/pull/239).

<BR />


### Year 2036 issue when used with the Thunderbird [Lightning](https://en.wikipedia.org/wiki/Lightning_(software)) calendar

"Sirenetest" is defined with:

```
BEGIN:VEVENT
UID:4fa20001-8512-4acf-8284-17d99c0f12ae
DTSTART;TZNAME=CET:20000506T120000
DTEND;TZNAME=CET:20000506T121000
SUMMARY:Sirenetest
RRULE:FREQ=YEARLY;BYMONTH=5;BYDAY=1WE;UNTIL=21000509
TRANSP:TRANSPARENT
END:VEVENT
```

Which works up to and including the year 2035. From 2036 onwards the "Multiweek" & "Month" overview will switch from showing 12:00 to 13:00:

| 2035 "Month" view | 2036 "Month" view |
| --------------    | ------------ |
| <img src="https://i.stack.imgur.com/G7NBR.png" heigth="200" alt="2035 shows 12:00" /> | <img src="https://i.stack.imgur.com/9KuZJ.png" heigth="200" alt="2036 shows 13:00" /> |

The entry when opened:

| 2035 entry | 2036 entry |
| --------------    | ------------ |
| <img src="https://i.stack.imgur.com/8OxL0.png" width="400" alt="2035 shows 12:00" /> | <img src="https://i.stack.imgur.com/I2p99.png" width="400" alt="2036 shows 13:00" /> |


Fortunately looking at a "Day" or "Week" will show the entry at the right time, but the popup is still showing the wrong time:

| 2035 "Day" view | 2036 entry |
| --------------    | ------------ |
| <img src="https://i.stack.imgur.com/wFeTk.png" width="400" alt="2035 shows 12:00" /> | <img src="https://i.stack.imgur.com/FSWzM.png" width="400" alt="2036 shows 12:00" /> |



Defining and using a timezone ID instead makes no change to the issue:

```
X-WR-TIMEZONE:Europe/Copenhagen
BEGIN:VTIMEZONE
TZID:Europe/Copenhagen
BEGIN:DAYLIGHT
TZOFFSETFROM:+0100
TZOFFSETTO:+0200
TZNAME:CEST
DTSTART:19700329T020000
RRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=3
END:DAYLIGHT
BEGIN:STANDARD
TZOFFSETFROM:+0200
TZOFFSETTO:+0100
TZNAME:CET
DTSTART:19701025T030000
RRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=10
END:STANDARD
END:VTIMEZONE

BEGIN:VEVENT
UID:4fa20001-8512-4acf-8284-17d99c0f12ae
DTSTART;TZID=Europe/Copenhagen:20000506T120000
DTEND;TZID=Europe/Copenhagen:20000506T121000
SUMMARY:Sirenetest
RRULE:FREQ=YEARLY;UNTIL=21000509;BYDAY=1WE;BYMONTH=5
TRANSP:TRANSPARENT
END:VEVENT
```

The Thunderbird Calendar Timezone preference is set to "Europe/Copenhagen".

*Note*: This issue has not been reported to Thunderbird.

<BR /> 


### Motivation

I could not find a single Danish online `.ics` calendar that was valid for the year 2022, so I decided to make one for the entire century. I hope to outlive it. I promise, if I do, I will make one for the next century too (-:
