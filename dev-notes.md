## important links

* MDN Article on the Web App Manifest (includes List of all Properties)
  *  https://developer.mozilla.org/en-US/docs/Web/Manifest 
* Web App Manifest - Browser Support: 
  * http://caniuse.com/#feat=web-app-manifest
* A detailed Web App Manifest Explanation by Google: 
  * https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/
* More about the "Web App Install Banner" (including Requirements): 
  * https://developers.google.com/web/fundamentals/engage-and-retain/app-install-banners/



## manifest.json

* to make the app installable.
* added to root dir. Where index.html is.
* <link rel="manifest" href="..."> is added to EVERY html file that the project uses.
* JSON
{
  .....
  .....
}

* manifest properties (all in " ")
  * name: "..." > long name of the app
  * short_name: "... " > name on the mobile, icon name
  * start_url: "/index.html" > which page to load on startup
  * scope: "."  > which pages are included in "PWA experience". "." means all pages in public folder are included.
  * display: 
    * "standalone": > should it look like a standalone app? "standalone" is default.
    * "fullscreen": > full screen, not common for web apps.
    * "minimal-ui"
    * "browser" : > like a normal web page in browser.. not native-app-like
  * background_color: "#fff" > background whilst loading and on splashscreen
  * theme_color: "#3F51B5" > theme color (e.g. on top bar in task switcher)
  * description: "a simple instagram clone, implementing a lot of PWA love" > desc.
  * dir: "ltr" > read direction of your app. ltr: left to right
  * lang: "en-US" > main lang of the app
  * orientation: "portrait-primary" > set and enforce default orientation. Doesnt rotate when the device rotates.
    * "any"
    * "portrait"
    * "landscape"
  * icons: [ {...} ] > config icons
    * src: >icon path
    * type: "image/png" 
    * sizes: "48x48"
  * related_applications: [ {...} ] > related native applications
    * platfrom: "play"
    * url
    * id

## emulator
* android studio kullanılıyor.
* instructor'ın bu konuyla ilgili yazılı notu:
Preparing the Emulated Device for ALL PWA Features
In the previous video, we set up an emulated Android device to test the PWA - this is optional.

Here are some more details about the process and how to prepare the device for the rest of the course though.

Setting up Android Studio:

In case you don't have Android Studio installed, make sure to do so. It's free!

You can download it from this URL: https://developer.android.com/studio/index.html

We only install it to get easy access to the Android Virtual Device (AVD) Manager though. You can access that Manager under "Tools" => "Android" => "AVD Manager". 

Detailed instructions on how to create a device with it can be found here: https://developer.android.com/studio/run/managing-avds.html

Updating Chrome on the Virtual Device

With an emulated device up and running, you're well-prepared to test your manifest.json file. For other features you learn about in this course, the pre-installed Chrome browser is too old though (at least at the point of time this course is created).

You can easily update Chrome on your virtual device though. Get an updated APK (basically the app installation file) from this link: https://www.apkmirror.com/apk/google-inc/chrome/#variants

Feel free to choose the latest one, download and install it. Give the device the permission to install from "unsafe" sources. If it fails, try a different APK version._