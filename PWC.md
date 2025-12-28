# PWController

Desktop app for `PerWiber` project, where managing songs and playlists happens.

## In-app usage

App has 2 parts, both shown on 1 screen, each having separate (althougth same paths) navigation.

### Playlists part

`Dark pink` background on right half.
Shows list of playlists.
On clicking specific playlist, **present** songs are displayed where clicking them will **remove** them.
There is also an option for **renaming** and **deleting** playlist or showing all songs,
also with option to **add** / **remove** them by simple click.

### Songs part

`Dark blue` background on left half.
Shows list of songs.
On clicking specific song, options will show:

- **deleting**
- **renaming**
- **downloading file** locally
- **reuploading file**
- **changing lyrics**
- **adding / removing** from playlists
- **cloning** to other listener will show

Also if there are no lyrics present, internet browser with searched song's name will open.
Or if the song is instrumental, button for it is there too.

### their options:

2 big buttons at top of both sections:

- `add`: Create **song** / **playlist**
- `search`: Search for specific **song** / **playlist**
- - case-insensitive, degrammarized

### Divider

Black bar in the middle.
Clicking it will navigate both playlists and songs part to their homepage.

In center, there is a list of all **listeners**, clicking one will display one's playlists and songs.

There is also an option for:

- Filtering only songs that **don't have lyrics**
- Displaying **missing** / **useless** song files in storage
- **Adding** listener
- Setting **favourite authors** for picked listener

![PerWIber controller logo](./usedImages/PWC.png)
