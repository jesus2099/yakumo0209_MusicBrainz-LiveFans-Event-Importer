# MusicBrainz: LiveFans Event Importer

A collection of Tampermonkey userscripts that helps transfer live event information from LiveFans.jp to MusicBrainz.

The goal of this project is to make it easier to add Japanese live music events to MusicBrainz and help improve its coverage of Japanese live music.

## Features

This project consists of two userscripts.

### 1. LiveFans-to-MusicBrainz-Event-Importer

Extracts event information from LiveFans event pages and tour pages and prepares MusicBrainz event creation forms.

The script supports:

- Individual event pages
- Tour pages with multiple scheduled events

For individual event pages, the script can retrieve:

- Event name
- Event date
- Start time
- Venue name
- Performer names

For tour pages, the script can retrieve:

- Tour name
- Performer names
- Scheduled event dates
- Start times
- Venue names
- Individual LiveFans event page URLs

Before opening MusicBrainz, the script displays a preview of the retrieved information so you can check it.

For individual event pages, the event name, date, and start time are passed to the MusicBrainz event creation form.

For tour pages, the script displays the available dates and allows you to select which events to import. The selected events are opened in MusicBrainz event creation forms sequentially.

The original LiveFans event page URL is also added to the edit note as a source.

### 2. LiveFans-to-MusicBrainz-Relationship-Helper

Works together with the Event Importer on the MusicBrainz event creation page.

It helps prepare relationship entries for:

- Venue
- Main Performer(s)
- Tour Series

The script processes each relationship one at a time.

It fills in the relevant information and relationship type, but you must select the correct entity from MusicBrainz's suggestions.

For tour events, the helper can prepare a relationship to the corresponding Tour Series.

The relationship must be reviewed and completed manually before submitting the event.

## Requirements

- A desktop web browser
- Tampermonkey
- A MusicBrainz account for submitting edits

## Installation

Install both userscripts in Tampermonkey.

1. Open the userscript file you want to install.
2. Click the Raw button on GitHub.
3. Tampermonkey should display an installation prompt.
4. Review the script and click Install.
5. Repeat these steps for the other userscript.

### Userscripts

- `LiveFans-to-MusicBrainz-Event-Importer`
- `LiveFans-to-MusicBrainz-Relationship-Helper`

Both scripts need to be installed for the complete workflow.

## How to use

### Step 1. Open a LiveFans page

Visit a supported LiveFans.jp page.

The Event Importer runs automatically on supported pages.

Supported pages:

- Individual event pages
- Tour pages

### Step 2. Check the event information

A preview panel appears in the bottom-right corner of the page.

For individual event pages, check the retrieved information:

- Event Name
- Date
- Time
- Venue
- Performer

For tour pages, check:

- Tour Name
- Performer
- Scheduled dates
- Start times
- Venues

On tour pages, select the events you want to import.

If the information looks correct, click **Open in MusicBrainz**.

If any information is missing or incorrect, check the original LiveFans page and be prepared to correct it manually in MusicBrainz.

### Step 3. Check the MusicBrainz event form

A new tab opens with the MusicBrainz event creation form.

The event name, date, and start time should already be filled in.

For tour pages, the tour name is used as the event name for the imported dates.

The original LiveFans event URL is included in the edit note.

When importing multiple dates, the script opens the selected event creation forms sequentially.

### Step 4. Add venue, performer, and tour relationships

If the Relationship Helper is installed, an Add Relationship panel appears on the MusicBrainz event creation page.

Click the button to process each relationship.

**Venue**

The venue name is entered into the relationship target field.

Select the correct venue from MusicBrainz's suggestions.

**Main Performer**

The relationship type is set to Main Performer, and the performer name is entered into the target field.

Select the correct artist from MusicBrainz's suggestions.

**Tour Series**

The helper prepares a relationship to the corresponding Tour Series using the imported tour name.

Select the correct Series from MusicBrainz's suggestions.

If the Tour Series does not exist on MusicBrainz, it must be created separately before the relationship can be completed.

Repeat until all available relationships have been processed.

### Step 5. Review and submit

Before submitting the event:

- Check the event name and date.
- Check the start time.
- Confirm the correct venue.
- Confirm all performers and their relationships.
- Confirm the correct Tour Series, if applicable.
- Review the edit note and source URL.
- Make any necessary corrections.

The scripts assist with data entry; they do not automatically submit edits to MusicBrainz.

## Important notes

- The scripts rely on the page structure of LiveFans.jp and MusicBrainz. Changes to either website may affect their functionality.
- Automatically retrieved information may be incomplete or incorrect. Always verify it against the source.
- MusicBrainz entity suggestions must be checked manually to avoid linking the wrong venue, artist, or Series.
- Tour Series relationships require the corresponding Series to exist on MusicBrainz.
- The scripts do not automatically create Tour Series or submit relationships.
- When importing multiple events, the script opens the selected MusicBrainz event creation forms sequentially.
- Please follow the MusicBrainz Editing Guidelines when creating event records.
- LiveFans.jp is used as an information source. Please respect its terms of use.

## Contributing

Contributions, bug reports, and suggestions are welcome!

If you find a problem or have an idea for improvement, please open an issue in this repository.

You can also help by adding and improving Japanese live event records on MusicBrainz.

Even small contributions help make Japanese live music history more accessible.

## Links

- [LiveFans.jp](https://www.livefans.jp/)
- [MusicBrainz](https://musicbrainz.org/)
- [MusicBrainz Events](https://musicbrainz.org/doc/Event)
- [Tampermonkey](https://www.tampermonkey.net/)

## Author

Created by [yakumo0209](https://github.com/yakumo0209).
