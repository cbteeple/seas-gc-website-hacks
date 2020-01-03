# seas-gc-website-hacks
All of the hacks I've done to make the [Harvard SEAS-GC website](https://gc.seas.harvard.edu/) look decent.


## Dependencies:
- Use the [OpenScholar](https://openscholar.harvard.edu/) Website Framework.
- A LOT of patience.

## Usage
Each of these files contains a custom widgit designed to work within the OpenScholar framework.

### Local Testing
1. Keep everthing in the same folder, and include the main style sheet:
``` html
<link rel = "stylesheet" type = "text/css" href = "main.css" />
```
2. Edit the files in a text editor (may I sugest [Sublime](https://www.sublimetext.com/)).
3. View the HTML files in Chrome, and use the developer panel to inspect them.

### Update Widgits
To update widgits in OpenScholar:
1. "Edit" the widgit
2. Copy and paste in the new version of the code
3. Apply changes

This workflow absolutely stinks, but it's the only way you can actually see changes inside of the OpenScholar framework. This is important to test becasue **OpenScholar does strange things with CSS**.

## Known Issues:
1. There are only a few external services from which you are allowed to load scripts and stylesheets. The ones I currently use are:
    - Various Google API's (Sheets, Calendar)
    - JQuery (stored on Google's servers)
2. CSS bahves strangely sometimes becasue OpenScholar uses the `!important` designation occasionally. Things are also often nested inside several divs for no reason. It's really imarative that you check what things will look like inline.


## Widgit List
 - **main.css** - All of the custom CSS classes used for all the various widgets
 - **about_us.html** - A custom "[About Us](https://gc.seas.harvard.edu/about_us)" page
 - **ama_dd.html** - Live display of a google form for the ASk-Me-Anything events with Dean Doyle. There's no moderation, so this may be deprecated soon
 - **calendar_agenda.html** - A custom skin for google calendars showing the [next 7 events in a nice list](https://gc.seas.harvard.edu/)
 - **calendar_full_responsive.html** - A custom skin for google calendars showing a [nice full-month calendar on large screens, or the event list on small screens](https://gc.seas.harvard.edu/calendar-pretty).
 - **SEVERAL SMALL WIDGETS NOT INCLUDED YET** - There are a bunch of tiny widgets on the website that rely on the **main.css** file to work. I'm working on transfering those here.
