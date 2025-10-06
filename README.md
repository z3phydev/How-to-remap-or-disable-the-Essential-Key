# How to remap (or disable) the Essential Key

A step-by-step guide to **disable or remap the Essential Key** on CMF and Nothing phones.

---

## Requirements

- CMF or Nothing phone that has an Essential Key 
- USB cable with data transfer capabilities
- Windows PC
- ADB tools (in this repo)
- [Keymapper App](https://play.google.com/store/search?q=Keymapper&c=apps&utm_source=emea_Med) (Only if you'd like to remap)

---

## Step 1: Prepare Your Phone

1. Enable **Developer Options**:  
 - Go to `Settings > About phone > Build number`  
 - Tap until a developer mode is enabled
 - You will see this by a popup saying "You are now a developer!" or "You are already a developer"
 - If you see "Developer Mode is not allowed for this user" then it means your device has restrictions that prevent enabling Developer Options and you will not be able to continue

2. Enable **USB Debugging**:  
 - Go to `Settings > Developer options > USB Debugging`  
 - Turn it on  


## Step 2: Install ADB Tools

1. Download the `platform-tools.zip` from this repo  
2. Extract it to a folder on your PC

## Step 3: Use ADB via Terminal

1. Open a terminal or command prompt in that folder  "C:\...\platform-tools"
> if you don't know how to do this navigate to the folder you exracted the zip to in file explorer and in the bar next to search type cmd

## Step 4: Connect Your Phone

1. Connect your phone via USB  
2. Verify connection by typing in the terminal:  
   ```bash
   adb devices
   ```
   
3. If it nothing comes up switch cable
4. If somthing does and says unauthorized after a string of letters and numbers you may have to allow you PC access by the notification that you (hopefully) got

## Step 5: Disable the Correct Package
1.Type or copy this command into your terminal:
```bash
adb shell pm disable-user --user 0 com.nothing.ntessentialspace
```

2. Hit enter and you should see an output that says "Package com.nothing.ntessentialspace new state: disabled-user"
3. Type or copy this command into your terminal:
```bash
adb shell pm disable-user --user 0 com.nothing.ntessentialrecorder
```

4. Hit enter and you should se an output thta says "Package com.nothing.ntessentialrecorder new state: disabled-user"

## If you don't want to use it at all Well done! you have successfully disabled The Essential Key

## If you would like to remap it to a different funtion continue to Step 5

## Step 6: Remap
1. Click [this link](https://play.google.com/store/search?q=Keymapper&c=apps&utm_source=emea_Med) and download Keymapper to your phone or go to the play store and download it there
2. If there are warnings at the top of your screen go through and fix them if need be
3. Tap the "+ New key map" button
4. Then tap "Record trigger" and press your Essential Key (if you get an unrecognized keycode just tap "Understood")
5. From there on select your Trigger type
6. Go over to the "Actions" Tab and add an action. You can make this do pretty much anything
7. Some actions require permissions so just enable them
8. If you would only like it add some Constraints
9. Make sure it's Enabled and Tap "Done"

## Congratulations! The Essential Key is now remapped to your chosen action. You can always go back and adjust it anytime.

If this guide helped you, consider giving the repo a star!
If something didn’t work, you have suggestions, or you just want to help improve this guide, please open an issue.
