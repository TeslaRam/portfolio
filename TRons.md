# TRons

> TeslaRam's add ons

## KMP project containing:

- usefull funs for various data types
- defaultly stylyzed composables
- basic commonly used strings
- view model processing functions and unifiers
- Data/Info obtaining state support
- Theme simplifiers / helpers
- default:
- - colors
- - dimens
- - typography (in future)

## IMPORTANT:

Call `setTRonsColors()` for setting colors used in many functions.

Call `setDefaultFont()` for setting up wanted default font.
> Call it before setting up fonts/theme

### Desktop:

Call `Toast.Init()` and `DialogFullWidthOps.Init()` for creating interface for desktop toasts and dialogs.

```
Window() {
  Box(modifier = Modifier.fillMaxSize()) {
    Toast.Init()
    DialogFullWidthOps.Init()
    ...
  }
}
```

---

Without this, app may crash

## Usage:

*latest version:* `2.0`

**KMP**: implementation("tr.trons:TRons:$version")

**Android**: implementation("tr.trons:TRons-android:$version")

**Desktop**: implementation("tr.trons:TRons-desktop:$version")

When using implementations in `androidMain + commonMain` *(KMP)*,
**before compilation**, you need to remove implementation from `commonMain` and sync,
in case of `Duplicate class` error.

`jvmMain` don't have this problem.

---

## TODO:

- typography
- akaya font
- card layout fix

![TRons](TRons_logo.png)
