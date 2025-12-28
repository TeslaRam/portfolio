# PWAndroid

Player for `PerWiber` project, where playing songs on android device happens.

I'm using `mediaPlayer` for playing songs, `retrofit2` for communication with **PWBackend** and
`room` with `SharedPreferences` for storing local history.
Whole app is in `Kotlin`'s framework `Jetpack Compose`.

## Rollable menu

> Menu can be **opened** / **closed** either by button in **bottom right** corner, or by swiping
> through screen

### Most played

**Top 5** most played songs and authors.
There is also statistics for total number of _songs_ and _different authors_ played.
If you want, you can evaluate how much _time_ of songs you have downloaded.

### History

Shows history of playtime of current session.

### Temps

Temporary playlists, here you can pick **name**, **songs** and most importantly
**time utill deletion**.

### Listeners

Pick current listener and set what listeners to download.

### Sync

Synchronize local storage with database. Download songs by specified listeners (settable in
#Listeners), delete useless files, store new settings locally.

### Quit

Turns off bluetooth, cancels notification and quits app.

## Main buttons

> Some options are visible from **main** screen, some are visible only when **menu is open**.

### Songs

List of songs, ordered from _newest_

### Shuffled

List of songs, _randomly reshuffled_ on each app start

### Playlists

List of playlists, sorted _alphabetically_.
There is also divided space for **temp playlists** if present.

### Authors

List of authors, ordered _alphabetically_, filtered by _number of songs_ from each author.

### Authors combinations

List of combinations of each author, minimum **3** songs from each author, ordered by _highest
number_ of songs.

### Search

Option to search for song by either **name** or **lyrics**

![PWAndroid logo](/usedImages/PWA.png)
