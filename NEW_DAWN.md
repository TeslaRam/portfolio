# NEW DAWN - `SK/CZ` - mobile

![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")

## Content:

- [Change of SK/CZ build](#change-of-skcz-build)
- [Navigation](#navigation)
- [User Level](#user-level)
- [Export](#export)
- [History](#history)
- [TODO](#todo)

---
---

## Change of `SK/CZ` build

### Will be changed:

- app name
- Api URLs
- default language

### How to change:

- in `root` directory is file `envConfig.properties`
- (un)comment wanted config and comment others (fallback = `SK`)

example for `SK` build:

```
wantedConfig=SK
# wantedConfig=CZ
```

- then sync gradle
- changes will be applied automatically on next build

## Navigation

> nav managment file: `navigation/AllDestinations.kt`

change `startDest` for initial screen
(`val startDest = HOME` recommended)

---

add destination to `disabledPaths` for disabling specific screen

```
val disabledPaths = 
	listOf<AllDestinations>(
		FINDINGS,
		SHARE_RIDE,
		SHARED_DATA_MANAGEMENT,
		CHAT,
		HOLY_MASS_SHARE,
	)
```

if submenuHolder item have no items, it will automatically hide

## User Level

> Specific levels of user permissions

`FoodCheck` **doesn't** depend on `UserLevel`, only `ADMIN` can select who is eligible to do it

### ANONYM

- default state, when not logged in
- can access main program and `CONFERENCE` section

### PILGRIM

- lowest state of logged in
- every registered pilgrim can log in with his id (NFC / db id)
- access to `NEWS` section

### VOLUNTEER

- for pilgrims, that want to help us with small things

### ORGANIZER

- for our team
- access to `ORGANIZER` section

### LEADER

- only for few specified people, team leaders
- access to `LEADER` screen
-
- create posts and notifications
-
- modify contacts and team data

### ADMIN

- for programmators
- access to `ADMIN` screen

## Teams

> This feature is still in it's begginings and will be enhanced in future

Volunteers are organized in teams.

Admin can set person's team database-wise.

That person will have shown only his `Team's data`.

In future, notifications will be reworked team-wise too.

## Export

### APK

> for quick share (for exapmle through Google Disk)

- `Build -> Generate App Bundles or APKs -> Generate APKs`
- Wait for build to finish
- Notification will be received:

```
Build completed successfully for 1 module:
Module 'New_Dawn.app': locate or analyze the APK.
```

- click `locate` or navigate manually:
  `.../NewDawn/app/build/outputs/apk/debug`
- find `.apk` file and share it :)

---

### Bundle (.aab)

> for Google Play release

[official tutorial](https://developer.android.com/studio/publish/app-signing#:~:text=In%20the%20menu%20bar%2C%20click,as%20shown%20in%20figure%202.)

- `Build -> Generate Signed App Bundle or APK -> Android App Bundle`
- Create new `Key store path` or use existing (can be misleading)
- fill in neccesary info (`Key store password`, `Key alias`, `Key password`)
- `Next -> release -> Create`
- Wait for build to finish
- Notification will be received:

```
App bundle(s) generated successfully for module 'New_Dawn.app.main' with 1 build variant:
Build variant 'release': locate or analyze the app bundle.
```

- click `locate` or navigate manually:
  `.../NewDawn/app/release`
- find `.aab` file and GLHF uploading it on GPlay :)

---
---
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")
![NS development logo](/usedImages/readmeFiles/readme_logo.png "NS development logo")

## History

<details>
  <summary>Show history</summary>

In `SK` conferention's early years, there was java app created
by [Grandik7](https://github.com/Grandik7), supporting only `FoodCheck`.

In 2023, [TeslaRam](https://github.com/TeslaRam) wanted to participate somehow, and asked whether he
can create app.
He got permission and contact to original app developer in february 2024.

Firstly, original sources were analyzed and reprogrammed to kotlin.
Later on, navigation has been added, and since then a lot of new options were unlocked.
Development team met and created template for `UserLevels`.
![template for `UserLevels`](/usedImages/readmeFiles/readme_history_8.png "template for
`UserLevels`")
![php scripts growing](/usedImages/readmeFiles/readme_history_3.png "php scripts groging")

For app's first year, it was planned to be released only for team, test it there and then year later
to release it for all visitors.
But reality didn't meet expectations, and there were only few people who provided interest in app.

But one of them was [MartinMikita](https://github.com/MartinMikita), `CZ`'s New Dawn developer.
He organized `SK` New Dawn leader and developers meet, and after further talks, he was introduced to
`SK` system and allowed to use app.

After `SK` conferention, [MartinMikita](https://github.com/MartinMikita)
and [TeslaRam](https://github.com/TeslaRam) had 1 month to combine these 2 different systems.
They worked, had online meetings and 4 days before `CZ` New Dawn they met in Brno for final works.
They created `envConfig` system, made large enhancements of data structures and joined 2 systems
into 1 app.
![combining systems in Brno](/usedImages/readmeFiles/readme_history_6.png "combining systems in Brno")

In `CZ` New Dawn, app was warmly welcomed and few funny upgrades were built during conferention,
most notably `Mňam Mňam`.

But there was problem, that they didn't have enough time together, so only few basic functionalities
were implemented in `CZ` version.
So year later, [TeslaRam](https://github.com/TeslaRam) documented API (very lightly), and we will
see what future brings.

![development image 1](/usedImages/readmeFiles/readme_history_1.png)
![development image 2](/usedImages/readmeFiles/readme_history_2.png)
![development image 4](/usedImages/readmeFiles/readme_history_4.png)
![development image 5](/usedImages/readmeFiles/readme_history_5.png)
![development image 7](/usedImages/readmeFiles/readme_history_7.png)
![development image 9](/usedImages/readmeFiles/readme_history_9.png)
![development image 10](/usedImages/readmeFiles/readme_history_10.png)

</details>
