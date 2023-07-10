<p align="center">
 
<img width="600px" src="https://github.com/wuseman/Android_12_FRPBypass/assets/26827453/447b0e4f-916d-471f-8cca-16007f7e771a" />
  <h3 align="center">(Works on all Samsung devices until Security Patch: <i>2022-02-01)</i></h3>
</p>

<center>More information about the CVC from Samsung can be found [here](https://security.samsungmobile.com/serviceWeb.smsb).</center>

No worries, I've got you covered with a newer version (they are fast but not fast enough, so I decided to share this wiki with the public). This hack works perfectly for all Samsung devices with the latest security patch (2022-02-01). While the wiki was created on February 21, 2022, it still works awesomely. Please note that this method does **NOT** work on Android 11. If you have an Android 11 FPR locked device, you can upgrade to the latest firmware from Samsung.

I'm sharing this information freely because it's fun and because I can, and because I believe it's enjoyable to share knowledge. I never report exploits or security issues for money. For me, time is more valuable than money.

#### 1) Power on your device with `Android 12` installed.

#### 2) Press `start` at the welcome screen.

#### 3) Press `End user license agreement` and proceed.

#### 4) Select a `Wi-Fi network`.

#### - Now connect to Wi-Fi...

#### 5) Press `volume up` + `power button`.

#### 6) Swipe your finger from the bottom `left` to `right`, then `up`.

#### 7) Allow talkback to record audio: `Choose only this time`.

#### 8) Remove the `always show` message in the popup window.

#### 9) Now press on: `use voice commands`.

#### 10) Allow talkback to record audio: `Choose only this time`.

#### 11) Say **slowly:** `Google Assistant`.

#### 12) Bixby will start.

#### 13) Login to your Samsung account.

#### 14) `Accept agreements`.

#### 15) Press cancel when Bixby asks for a faster way to sign in.

#### 16) Press `start`.

#### 17) Say: `Open Google Chrome`.

#### 18) Press `Accept and Continue`.

#### 19) Press "no thanks" on `turn on sync`.

#### 20) Browse to [Nr1](https://www.nr1.nu/wiki/adb/readme/).

#### 21) Scroll down to "`Alliance Shield X (Galaxy Store)`".

#### 22) Install "`Alliance Shield X (Galaxy Store)`" from the Samsung Store.

#### 23) Once done, open the `Alliance Shield X Application`.

#### 24) Press `Next` in the welcome window.

#### 25) Press `Next` again in the permission window.

#### 26) Press `Next` in the privacy promise window.

#### 27) Press `Got It` to get started.

#### 28) Login to your account.

#### 29) Enter the DEVICE Name. I tried this hack with an `SM-G975F` + `SM-G985F`.

#### 30) Enable `Device Admin` in the device setup screen.

#### 31) Press `activate` in the `activate` device admin application.

#### 32) Press `Next`.

#### 33) Enable Knox in the Samsung Knox window, press `next` (don't remember exactly right now).

#### 34) Press continue in "`Knox License Activation`".

#### 35) You should see "Knox license validation completed".

#### 36) Press `next`.

#### 37) Press `finish` in the import window.

#### 38) Press `app manager` in the upper-left corner.

#### 40) Press `service mode`.

#### 41) Press `activities`.

#### 42) Press `service mode`.

#### 43) Press `open in the popup window`.

#### 44) Choose `MTP+ADB` and press `OK`.

#### 45) Accept the `adb request` on your phone.

* Now, via `adb`, execute the following command on your device:

```bash
content insert --uri content://settings/secure \
  --bind name:s:user_setup_complete \
  --bind value:s:1
```

* For those interested in a deeper understanding, the logcat provides the following information:

```
02-20 23:25:40.306   936  8470 D RestrictionPolicy: isSettingsChangesAllowedAsUser, userId 0: true
02-20 23:25:40.306   936  8470 D SettingsProvider: ret = 1
02-20 23:25:40.318   936  8470 I GenerationRegistry: mBackingStore.isClosed(): false
02-20 23:25:40.320  5655  5655 I AODSettingsHelper: content://settings/secure/user_setup_complete changed
02-20 23:25:40.322  5655  5655 I AODSettingsHelper: mKey=user_setup_complete, mIntValue=1, mStringValue=null
02-20 23:25:40.322  5655  5655 I AODSettingsHelper: onChange() COMPLETED elapsed= 2
02-20 23:25:40.322  5655  5655 I AODSettingsHelper: **#### onSettingsValueChanged for content://settings/secure/user_setup_complete
02-20 23:25:40.322  5655  5655 I AODSettingsHelper: **#### onSettingsValueChanged callbackList == null
02-20 23:25:40.323   936  1133 D PackageManager: SetupWizardFinished: true
02-20 23:25:40.323 17664 17664 D hw-ProcessState: Binder ioctl to enable oneway spam detection failed: Invalid argument
02-20 23:25:40.325 17664 17664 D AndroidRuntime: Shutting down VM
02-20 23:25:40.344  5655  5655 I AODSettingsHelper: content://settings/secure/user_setup_complete changed
02-20 23:25:40.346  5655  5655 I AODSettingsHelper: mKey=user_setup_complete, mIntValue=1, mStringValue=null
02-20 23:25:40.346  5655  5655 I AODSettingsHelper: onChange() COMPLETED elapsed= 1
02-20 23:25:40.346  5655  5655 I AODSettingsHelper: **#### onSettingsValueChanged for content://settings/secure/user_setup_complete
02-20 23:25:40.346  5655  5655 I AODSettingsHelper: **#### onSettingsValueChanged callbackList == null
02-20 23:25:40.346  5655  5655 D DeviceProvisionedControllerImpl: Setting change: content://settings/secure/user_set
```

#### 46) Press `volume up` + `power`.

#### 47) Swipe your finger from the bottom `left` to `right`, then `up`.

#### 48) Slowly say: `Open Settings`.

#### 49) When Bixby launches, press `volume up` + `power` again to turn off Talkback settings.

#### 50) Press the `record` button.

#### 51) Now say: `Open Account Settings`.

#### 52) Press `add account`.

#### 53) Add your Google account.

#### You are now signing in without any issues.

#### 54) And you're in!! :)

* As you may notice, you are now signed in.

!!! alert "IT'S NOT DONE!!! DON'T JUST RUSH INTO A FACTORY RESET OR SOMETHING, CONTINUE READING..."

#### 55) Let's head back to the welcome screen. Turn back as many times as needed to get there.

#### 56) You can now press `next`, `accept license and policies`, and `wifi` should already be fixed, so press next. Now, you will see... nothing.

#### 58) IT STOPS! You won't be able to continue. `DON'T PANIC`!

#### 59) Once again, let's get `Bixby` started :)

#### 60) Press `volume up` + `power`.

#### 61) Swipe your finger from the bottom `left` to `right`, then `up`.

#### 62) Say `Google Assistant`. When Bixby launches, press `volume up` + `power` to turn off Talkback settings.

#### 63) When you hear the beep, slowly say: `Open Settings`.

#### 64) Go to the "Apps" section, which has been locked all the time until we added our Google account. You probably already tried opening the Settings application, and it crashed. But now it's unlocked.

#### 65) Scroll to the `One UI Home` application and open it.

#### 66) Press `Set Home Screen`.

#### 67) Select `One UI Home`, and when you press on it, `System UI` will launch, bypassing the earlier setup wizard.

#### 68) And it results in the screen below when you press on `One UI`:

* You have just hacked Samsung's latest security patch, and there are a thousand reasons why I do not use cell phones ;)

* Since adb shell is still open, clear all Samsung applications so we can take control over lock settings without any brute-forcing:

![](https://www.nr1.nu/hacking/android/Samsung_Galaxy.s10_plus_Android.v12.PREVIEWS/clear_all_samsung_apps.gif)
          
```bash
cmd package list packages \
  | cut -d: -f2 \
  | egrep samsung > /storage/self/primary/clear.txt 
```

```bash
sed 's/^/pm clear --user 0 /g' /storage/self/primary/clear.txt  \
  > /storage/self/primary/clear_script.sh 
```

```bash
sh -x /storage/self/primary/clear_script.sh 
```

```bash
cmd package list packages \
  | cut -d: -f2 \
  | egrep google > /storage/self/primary/clear_google_apps.txt 
```

```bash
sed 's/^/pm clear --user 0 /g' /storage/self/primary/clear.txt  \
   > /storage/self/primary/clear_google_apps.sh
```

```bash
sh -x /storage/self/primary/clear_script.sh 
```

Your lock settings are NOT disabled if you are using an FRP locked device. However, you can confirm this with the following command:

```bash
cmd lock_settings get-disabled
```

cmd lock_settings is the new way we used locksettings in the past (you probably saw my wbruter script, which is very old and slow nowadays, use cmd instead). And since lock_settings was introduced in cmd, we can simply use the following command to disable the lock screen without any hacking:

```bash
cmd lock_settings set-disabled true 
```

Since we still love ADB and prefer working in the command-line interface (CLI) rather than the GUI (Graphical User Interface), let's proceed with the following steps:

#### Set your PIN code using the following command:
```bash
cmd locksettings --set-pin XXXX XXX
```

#### For GUI enthusiasts, you can open the settings and browse to "Biometrics and Security" either with the command below or through your home screen:
```bash
am start -a android.settings.SETTINGS
```

#### Add your fingerprint and enable face recognition, then set your PIN.

Congratulations! You have successfully hacked the latest Security Patch from Samsung (2022-02-01).

This tutorial is licensed under the GNU General Public License v3.0. Please refer to the [LICENSE.md](https://www.nr1.nu/linux/license/) file for details. Feel free to copy this wiki, but if you do, please share the URL to this original post. Thank you!

Happy hacking, and never give up!
