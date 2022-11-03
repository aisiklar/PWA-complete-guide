
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
  * short_name: "... "
  * start_url: "/index.html" > which page to load on startup
  * scope: "."  > which pages are included in "PWA experience". "." means all pages in public folder are included.
  * display: "standalone": > should it look like a standalone app? "standalone" is default.
  * background_color: "#fff" > background whilst loading and on splashscreen
  * theme_color: "#3F51B5" > theme color (e.g. on top bar in task switcher)
  * description: "keep running until you're sweaty" > desc.
  * dir: "ltr" > read direction of your app. ltr: left to right
  * lang: "en-US" > main lang of the app
  * orientation: "portrait-primary" > set and enforce default orientation
  * icons: [ {...} ] > config icons
    * src: >icon path
    * type: "image/png" 
    * sizes: "48x48"
  * related_applications: [ {...} ] > related native applications
    * platfrom: "play"
    * url
    * id