# Google Analytics

## Task
Install Google Analytics tracking to page and track how many people have
downloaded the resume and build the resume download section.

## Plan
The project will be divided into 4 parts. The parts are research/relearn,
implementation, fine tuning / bug fixes (if needed) & documentation.
For each part, there is one day reserved and 5th day is the release date.

### Details:
- Length: 5 days
- Start: 3.12.2021
- Deadline: 7.12.2021 1pm (CET)

### Google Analytics Setup
- It should track views, resume download times (all and unique) and tag
manager could be used if needed to improve in future...

- There should be 2 views raw data and normal view with most relevant
and useful info

### Website Download Section
My vision for this section would be something like this:

![Sketch](/assets/download-section-sketch.jpg)

This should be okay for a simple download section.

## Implementation

### Website Download Section
Code:
![html-code](/assets/download-code.png)

Visual:
![html-download](/assets/download-section.png)

+Added Resume section to Navbar

### Google Analytics Setup
Inital Setup / Tryout:
1. Created the following:
  - New account
  - New Property
  - Select what sort of tracking to use


2. Copied property's Global site tag
3. Paste it to website
4. Push code to cloud to update site
5. Wait for update and visit site with "fresh" browser

Result:
![inital-analytics-setup](/assets/initial-js-result.png)

Now I know the JS-plugins, popper and analytics works.
The rest is about setting up specific event tracking and tag manager

### Tag Manager Setup
First, I did the basic setup (Create account and container).
After that I fiddled around a bit, played with the debug tool and
checked how the "new" Google Tag Manager and Google Analytics 4 worked together.


Note: The content was different from certification material


I ended up creating 2 tags and 2 triggers. First tag is for all basic Google
Analytics (tracks same things as original GA setup) and second one was for
resume download event.

Trigger used by 1st tag is all pages and the resume event uses click element
trigger with id and url path restrictions to limit it to activate only on
specific website and element.

Tags:
![tag-list](/assets/tags-list.png)

Resume Download:
![resume-download-tag](/assets/resume-download-tag.png)

Triggers:
![all-pages-trigger](/assets/all-pages-trigger.png)

![resume-download-trigger](/assets/resume-trigger.png)

### Problems

1. GA4 made many things learned from Google Academy "pointless". The fundamentals
are there but many things don't work like portrayed. Maybe some old accounts still
have that old system in place but fresh accounts seem to use GA4 to my knowledge...
2.  GA4 affected views so I don't know exactly as of now how it works now
(refer to planning phase on views)
3. Had a dumb mistake where the cv would not download but the issue was I forgot
the . from  href="./"



## Finished Job / TL;DR
Everything shows up in Google Analytics page and resume downloads have specific
event to show download numbers.

Demograph View:
![demograph-view](/assets/demograph-overview.png)

Tech View:
![tech-view](/assets/tech-overview.png)

In events section you can see the general download traker and different
naming versions of resume download. Current is called "resume_download_github".

Event View:
![event-view](/assets/event-overview.png)

System Overview:
![system-overview](/assets/system-overview.jpg)
