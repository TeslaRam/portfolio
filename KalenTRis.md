# KalenTRis

App for **my events**, events I **care about**, **namedays** and **Christian Feasts** with
_graphical representation_

> Supports both **Android** and **Desktop** environments

## In-app usage

### Date bar

> Row on top, which displays range of filtered dates

**Clicking** on bar opens _manual date options_.
Here you can pick

- Specific starting date (`dd.MM.yy`)
- Weeks covered (`Unsigned Int`)

Clicking again will hide _options_ and applies your date settings.

**Holding** bar sets and applies default values (`today` - `1 week`)

### Events list

List of _events_ happening between specified dates.
Between every week, there is small line to divide them visually.

Under them, there is displayed who has **nameday** in slovakia and **christian feast** for _starting
date_ (defaultly today).

Finally, there is errors list, where whole _untransformed_ line is written on red background, so
you know where the error is.

### Graphical icons

On bottom of the screen, there is graphical calendar.
7 lines per row (representing week).
First line starts with **starting date**, last line ends with end of month (of **last's date**).

Clicking any square, beneath calendar appears events for that day.

### Online / Offline support

When **online**, app has `blue` background and loads `current` data.

When **offline**, app has `green` background and loads `saved` data.

### Event's colors

- **Default** text has `white` color.
- **Important** one has `red` color.
- **Today** is marked with `yellow` color.

Graphical calendar has same colors but different rules:

- If in that day is **important event**, the box is `red`.
- If in that day is **event**, the box is `yellow`.
- **Other** boxes are `white`.

## Connected APIs

### FaZe CS2

> Using PandaScore https://www.pandascore.co/

Collects upcoming FaZe clan matches. `#FaZe Up`

### Kalendaris

> https://github.com/Damko757/kalendaris-api
>
> Created by my friend https://github.com/Damko757

Collects events specified by me.
They are in 2 _.txt_ files, `kalendar` and `kalendar-stale`, stored on my _Raspberry Pi_.
Stored in format `dd.MM.yy - data`.

Event's importance can be specified by 3 marks, written on start of the line:

- `_ (underscore)`:Show event only if it is **today**
- `- (dash)`: **Don't visualise** event on graphical calendar (will show with `white` color)
- `+ (plus)`: Mark event as **important** (`red` color)

### vut-tasker

> Friend's project https://github.com/Damko757/vut-tasker

Collects specific person's (mine) tasks and filters uncompleted.

### Namedays

> https://nameday.abalin.net/

Collects namedays from specific date, filtered to slovakia only.

### Christian feasts

> http://calapi.inadiutorium.cz/

Collects christian feasts of specific date, in english language.

![KalenTRis logo](/usedImages/KalenTRis_logo.png)
