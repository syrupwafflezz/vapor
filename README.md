# Vapor - a GUI framework for FTEQW.
Made by wither. A big thank you to Jaycie, Spoike, Shpuld, and eukara for support, inspiration, feedback and testing.
## What is Vapor?
Vapor is a GUI framework for FTEQW which was made with the intention of being an easy-to-use, drop-in solution for any game built on FTEQW. Vapor's scheme data (where a window is, what stuff does it have, where is the stuff exactly within that window, etc.) is all in a .json file for ease of use. No QuakeC coding at all!
## Is it stable?
I would consider Vapor to be mostly stable, but there will be some stuff wrong with it as I have not done much testing on it, other than testing for basic functionality.
## Are you going to keep maintaining this?
Probably not. There's a lot of stuff I'd like to do in FTEQW and Vapor was just one of them. But I did spend a good amount of time in Vapor and I would rather release it as-is than not release it at all. I will most likely archive this repository once I am done uploading all of Vapor. I would strongly recommend you to fork Vapor and add/remove/clean up some of its code.
## What's the feature list?
Well...
- Build a functional menu with just .json data!
- Make a button, text, image, toggle, slider, combo, radio, text entry and action bind object with ease!
- Create a tab view of stuff that should only be seen when viewing a single tab! (i.e. hide everything that has nothing to do with "Video", and show everything that does)
- Customize the color scheme and mix-and-match to create a colorful menu!
- Easily build upon Vapor's foundation with a new object!
## Why did you pick the name Vapor?
Because Vapor's style and color palette is the same as Steam's early 2000's UI. Ergo, Vapor <-> Steam.
## WHERE THE F!@# IS THE DOCUMENTATION?!
There is none. Read the sample .json file then read the code to get a feel for what is actually going on in classic Quake mod fashion. Good luck, you're gonna need it! Hint: you can use the `-` operator to overload the `position` and `size` key of every object. For instance, `"position" : ["-0", "-0"]` would set a window to the *right* side of the screen, at the *bottom*, in contrast to `"position" : "["0", "0"]"`, which would set it to the *left* side of the screen, at the *top*. This goes for both a window, and an object which is a child of that window, in which case, the child would be set to the far right corner of the parent window, etcetera. The `size` key is similar, only that it will resize a window or object to be as big as the screen (in the case of the window) or as big as the parent (in the case of the child object, like a button)

In contrast, the `*` operator will position a window or object at the middle of the screen, or parent window in the case of the child object. Same logic as `size`
.
There is also a `condition` key which will check for the value of a given console variable and display the object in question if the check is a success. For example, say you don't want some text to appear if the game volume is lower than 0.75. To do so, you would attach `"condition": ["volume", "<", "0.75"]`.

If you want to show a window ONLY in the loading screen, then add the key `"show": "-1"`. Use `"1"` for when you want to show it ONLY when the game is not loading. Any other value will just hide the window regardless of context, which could be useful for testing I suppose.
## Usage
**Engine support other than FTEQW is non-existent. Do not even try using this on QSS or DP.**
Download the code and move menu.dat and data.json into your game's root directory. *menu.dat* is Vapor's actual QC code and *data.json* is Vapor's scheme/resource data. You don't really need much else.
## Build
You can execute "compile source/make.source" in FTEQW's console, otherwise, just use FTEQCC and select make.source as the source file.
## License
The license for Vapor is MIT. So go crazy with it. I don't particularly care.
