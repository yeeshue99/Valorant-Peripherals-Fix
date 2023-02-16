# Valorant Peripherals Fix
Valorant Vanguard seems to sometimes "eat" mouse and keyboard input; to the point where you are unable to click certain elements like tabs in a browser, or chats in Discord. I believe this can be triggered when holding shift or ctrl for long periods of time while in game, or from repeatededly pressing one of these buttons and unknown amount of times. This can still occur with Sticky Keys disabled and removed from the computer. 
I have found this cam be related to a software named Interception, but as someone who has never installed that program, that proved to be a dead end. I found [this link](https://www.reddit.com/r/VALORANT/comments/genkxg/comment/fppcf1x/?utm_source=share&utm_medium=web2x&context=3) that details a fix that can be done regardless of the installation status of Interception.

## What Happened?
In your registries, you have some values that seem to correspond with the control system of your mouse and keyboard. Valorant Vanguard, as a trigger to some unknown inputs, can swap these control registries, resulting in this issue. By simply reverting the registry keys to the correct values, this can be fixed. Since a computer restart seems to fix the registries, it seems like Valorant Vanguard reverts these values properly upon system refresh. This is important, as this fix can cause issues.

## The Fix
By running the file fix-registries.reg, the registry values will be automatically updated to the correct values. Therefore, it can be run anytime this issue is experienced. As mentioned above, since Valorant Vanguard reverts these values on system refresh, you may start you computer with values that were flipped again, causing you to be unable to log into your computer. As a result, it is strongly recommended to create a link to the registry script, and have this script run on startup. By doing so, the values will always be correct on startup, and you should experience no issues.

## Installation Instructions (HIGHYL RECOMMENDED)
1. Create a shortcut to `fix-registries.reg`.
2. Right click on the shortcut and click on `properties`.
3. Copy the entirety of the text in the `target` field.
4. Press `[WIN]+[S]` to open windows search.
5. Search `gpedit` and press `[ENTER]`. You should see it say "Edit Group Policy".
6. Navigate to `Local Compuetr Policy > Windows Settings > Scripts (Startup/Shutdown) > Startup`.
7. Add a new startup scrippt and navigate to the location of your shortcut.
8. In the `Parameters` section, type `/s` and then paste the file path you copied earlier. The end result should look like this: `/s C:\Path\To\Location\fix-registries.reg`
9. Click `Apply` then `Ok`

## Usage
Simply run fix-registries.reg whenever you run into issues.