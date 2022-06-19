# Vapor - a GUI framework for FTEQW.
Made by wither. A big thank you to Jaycie, Spoike, Shpuld, and eukara for support, inspiration, feedback and testing.
# What is Vapor?
Vapor is a GUI framework for FTEQW which was made with the intention of being an easy-to-use, drop-in solution for any game built on FTEQW. Vapor's scheme data (where a window is, what stuff does it have, where is the stuff exactly within that window, etc.) is all in a .json file for ease of use. No QuakeC coding at all!
# Is it stable?
I would consider Vapor to be mostly stable, but there will be some stuff wrong with it as I have not done much testing on it, other than testing for basic functionality.
# Are you going to keep maintaining this?
Probably not. There's a lot of stuff I'd like to do in FTEQW and Vapor was just one of them. But I did spend a good amount of time in Vapor and I would rather release it as-is than not release it at all.
# What's the feature list?
Well...
- Build a functional menu with just .json data!
- Make a button, text, image, toggle, slider, combo, radio, text entry and action bind object with ease!
- Customize the color scheme and mix-and-match to create a colorful menu!
- Easily build upon Vapor's foundation with a new object!
# Usage
**Engine support other than FTEQW is non-existent. Do not even try using this on QSS or DP.**
Download the code and move menu.dat and data.json into your game's root directory. menu.dat is Vapor's actual QC code and data.json is Vapor's scheme/resource data. You don't really need much else.
# Build
You can execute "compile source/make.source" in FTEQW's console, otherwise, just use FTEQCC and select make.source as the source file.
