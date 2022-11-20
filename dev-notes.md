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