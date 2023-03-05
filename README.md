# How do you uninstall an application?

I can uninstall an app by its package name. To obtain a list of all the packages installed on the device, run command <code>adb shell pm list packages</code>. To filter out the results by a keyword contained in the package name, use the <code>-f</code> option, as in <code>adb shell pm list packages -f <key_word></code>. 
      
Sometimes, package names change. To retrieve a list of 3-rd party packages, installed by the user (not OEM-pre-installed), include the <code>-3</code> option, as in <code>adb shell pm list packages -3</code>. All the vendor-preloaded apps that are shipped with the device live in the <code>/system</code> directory. All the apps that I, as a user installed, live in the <code>/data/</code> folder. The <code>-3</code> option directs the command to the <code>/data/</code> folder and returns all the apps that reside there.

 
The package name convention is usually <code>com.app.company.project</code>. [Once I know the package name](https://github.com/lana-20/android-package-name), I run command <code>adb uninstall <package_name></code> to uninstall the app by that package name. The expected output is <code>Success</code>, and the app is gone from the device.
