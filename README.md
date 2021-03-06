# Gamepad Viewer Nintendo Switch Pro Controller Skin
the odds of me updating this if anything on gamepad viewer changes enough to break it are very low <br/>
It's a repo for a thing!

This is a Nintendo Switch Pro Controller skin created for Gamepad Viewer that, afaik, only works if used inside of OBS studio**. <br/>
All images were made by me, Soveliss. <br/>
The CSS is based off that of the example custom CSS provided by the creator of gamepad viewer, and I also referenced the CSS behind skins by Million Lights and HawkyYT to help me understand what was going on (though it ended up being trial and error mostly) <br/>

This works by creating a browser source in OBS, linking it to "https://gamepadviewer.com/?p=1&s=1" <br/>
and then pasting the contents of the CSS file (Switch-Format.css) into the custom CSS box underneath that <br/>
Voila! <br/>
Here's a screenshot of what it looks like 22 feb 2022: <br/>
<img width="721" alt="Screen Shot 2022-02-22 at 4 43 02 PM" src="https://user-images.githubusercontent.com/99949632/155244134-a2c90936-07e0-4921-94f5-957d9663ed07.png"> <br/>
Note I set my browser window size to 630x528 pixels b/c that's the size of the images used, and I also usually limit the frame rate to 30 or 60 fps - there's no reason to record inputs more often than the game I'm playing is doing so, and it can also help fix it if the browser source starts lagging.

The Illustrator file included contains everything that's been exported to the basic assets as of some point (might not stay updated), should you wish to customize this and make your own repo with your own skins.
Each group in the Illustrator file can be exported as a .png at 1x resolution and renamed to the name of the group, then in the CSS you will need to change only the filepath to reach wherever you're hosting your files (the links should be obvious, if you make your own github repo then change them to https://raw.githubusercontent.com/username/repository/filepath/6thumbs.png or etc) <br/>
Exporting assets after moving anything, modifying sizes, modifying export sizes, or other changes besides color/inside clip groups/etc may require changes to the CSS to make it look right, no guarantees.<br/>
<br/>
<br/>

As for how to actually pull inputs from the switch... from what I've found there are basically 3 options for capturing inputs on switch: <br/>
1: open joystick & a system module installed on a hacked switch - requires a hackable switch, some confidence, and knowing how to safely run CFW online (and/or being okay with potentially being banned from Nintendo's online services) <br/>
2: any man-in-the-middle for a wired controller (even a wired pro controller) - this one seems feasible, until you realize that usb protocols are fairly hard to tap, and most solutions are basically homebrew on $80+ microcontrollers inbetween the controller and the console, making them both potentially more awkward and more expensive than the next option: <br/>
3: use a dualshock 4 lmao - it turns out playstation controllers (and afaik, ONLY playstation controllers) can connect to bluetooth and usb simultaneously and separately, allowing it to, for example, connect to a $20 bluetooth usb stick plugged into the switch's dock, and also be plugged in to your computer via usb, giving inputs to both at the same time

Why do only playstation controllers stack the connections like this? No clue. Other controllers will only output to one device or the other. Conveniently, the dualshock 4 and dualsense both also have gyros, making them functionally identical to the switch pro controller... plus a frame or two of motion input lag from having to be registered as a wired controller. Why Nintendo hasn't solved motion input being slower when wired after 5 years I really couldn't say, though.<br/>
<br/>
<br/>
\*\*It'll probably also work on google/etc if you know another way to make gamepad viewer actually read the css instead of trying to read it from rawgit... <br/>
That's because Gamepad Viewer assumes it can pull the repo's files from rawgit despite it being nearly 4 years out of service.
So it dead-ends there when attempted on the actual website, unless you're using an old enough skin (so it can be pulled from rawgit) or self-hosting the css somewhere besides github (so it doesn't try to pull from rawgit) (github.io might work but I'm too lazy to try) <br/>
