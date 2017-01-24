# PicoTOUCH

## :: Pico-8—*now in mobile flavor!*
The current Pico-8 HTML export does not support touch controls, nor is the webpage produced optimized for mobile.

This project aims to do a few things:

- Implement touch controls
- Beat the existing html into a responsive, mobile-ready webpage
- Add web-app functionality for iOS, allowing the page to be saved to the homescreen and used like a native app (complete with *sound!*), without all of the obstructive Safari UI.

## :: Usage
If you'd like to use PicoTOUCH to play your own Pico-8 games on mobile, good news—it couldn't be easier. 

1. Download the Master branch of this repo. 
2. Fire up Pico-8, load your game, and export it as html/JavaScript *(after loading your cart, enter "`export your_cart.html`" at the Pico-8 terminal screen)*.
3. Locate your exported files and copy the JavaScript file into the "`carts`" folder you downloaded in step 1. *(Since Pico-8 is already open, make it easy on yourself and enter "`folder`" into the terminal screen to have Pico-8 automatically show you were your exported files are.)*
4. In your downloaded PicoTOUCH folder, open "`picotouch.html`" in your favorite text editor, find the line of code near the top of the big "script" tag that reads "`cart.src = "carts/picomenu.js";`" and replace "picomenu.js" with the name of your game's JavaScript file *(the one you copied into the `carts` folder)*.

With that done, all that's left to do is host your PicoTOUCH folder somewhere, open your mobile web browser, and navigate to your domain!

*(Alternatively: if you, like me, don't have a spare domain and hosting service lying around, you can do all of the steps above on iOS using the wonderful "Textastic Code Editor" app, and play your game using it's handy-dandy "Preview in Safari" feature. While I'm sure this can be done on Android in a similar fashion, I don't have one, so you'll have to hunt for a similar app yourself.)*

## :: Known Bugs and Troubleshooting
### // ISSUE:
Sometimes, for reasons currently unknown, JavaScript files exported using the most current version of Pico-8 sometimes fail to load. This manifests as PicoTOUCH opening, the Pico-8 boot screen running, and then Pico-8 gets hung up and never actually runs the game—it just sits on the "`booting...`" message forever.

### // SOLUTION:
Presently, there are no sure-fire fixes. I have been able to get carts that fail to load running by simply deleting my export from everywhere and re-exporting again. That is to say, so far the problem has spontaneoulsy fixed itself at random, by way of magic.

In fact, if you have this issue and discover the cause or even the solution, I would greatly appreciate your report!

## :: Project Achievements
- The page is now responsive and looks very pretty indeed (*at least using an iPhone 7, which is all I have to test with.*)
- The page is web-app ready, and can be saved to the iOS homescreen and run just like an app—sound and all.
- Touch controls have been successfully implemented and are in a usable state, including the in-game pause function.
- Supports both portrait and landscape orientations.
- Supports phone and tablet screen sizes.
- Includes a curated 15-cart library.

## :: To-Do
### // Things to Fix
- Menu button on tablets in portrait mode.
- Layouts on non-iOS mobile devices.
- ~~Limit touch input to button areas.~~

### // Things to Add
- Prefer external audio.
- Mute button.
- Add the ability to change games on-the-fly without restarting the app/reloading the page.