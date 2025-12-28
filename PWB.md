# PWBackend

Backend part for `PerWiber` project, where storing and obtaining data happens.

Used database is `PostgreSQL`, used framework is `SpringBoot`.

## Listeners

This is my _identifier_ for accounts. I don't have specific table for listeners, just every playlist, song, ... has this
`listener` attribute, and when searching for elements, they are filtered by that.

## Songs storing

Songs are stored as `UUID.mp3`. Thanks to this, I'm sure that filename is unique, and at the same time i don't need to
work with song's name, so there is no need to name it more "humanly".

## Tables

### Song

Stored:

- Id
- Name
- Authors
- Listener
- Lyrics
- Time added
- Time edited

### Playlist

- Id
- Title
- Listener
- Songs

### Favs

Favourite authors, identified by `listener`-`author name` duo.

![PWBackend logo](./usedImages/PWB.png)
