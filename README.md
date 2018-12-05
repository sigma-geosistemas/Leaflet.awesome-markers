# Leaflet.awesome-markers plugin v2.0
Colorful iconic & retina-proof markers for Leaflet, based on the Glyphicons / Font-Awesome icons

Version 2.0 of Leaflet.awesome-markers is tested and works with the latest available versions:

* Bootstrap 3 (up to 3.3.7)
* Font Awesome 4.0 (up to 4.7.0)
* Ionicons 1.5.2
* Leaflet 0.5 (up to 1.0.3)

Use version 2.0.x for compatibility with the newer versions of bootstrap, font-awesome and leaflet.

Version 1.0 of Leaflet.awesome-markers is tested and works with:

* Bootstrap 2
* Font Awesome 3.0
* Leaflet 0.5

Use version 1.0.x for compatibility with the older versions of bootstrap, font-awesome and leaflet.

## Screenshots
![AwesomeMarkers screenshot](https://raw.github.com/lvoogdt/Leaflet.awesome-markers/master/screenshots/screenshot-soft.png "Screenshot of AwesomeMarkers")

<a href="http://jsfiddle.net/VPzu4/975/" target="_blank">JSfiddle demo</a> 

### Twitter Bootstrap/Font-Awesome icons
This plugin depends on either Bootstrap or Font-Awesome for the rendering of the icons. See these urls for more information:

For Font-Awesome
- http://fortawesome.github.com/Font-Awesome/
- http://fortawesome.github.com/Font-Awesome/#integration

For Twitter bootstrap:
- http://twitter.github.com/bootstrap/

For Ionicons:
- http://ionicons.com


## Using the plugin
- 1) First, follow the steps for including Font-Awesome or Twitter bootstrap or Ionicons into your application.

For Font-Awesome, steps are located here:

http://fortawesome.github.io/Font-Awesome/get-started/

For Twitter bootstrap, steps are here:

http://getbootstrap.com/getting-started/

For Ionicons:

Add the ionicon stylesheet from a [CDN](http://code.ionicframework.com/ionicons/1.5.2/css/ionicons.min.css) or [download ionicons](http://ionicons.com).
    
````xml
<link rel="stylesheet" href="http://code.ionicframework.com/ionicons/1.5.2/css/ionicons.min.css">
````

- 2) Next, copy the dist/images directory, awesome-markers.css, and awesome-markers.js to your project and include them:
````xml
<link rel="stylesheet" href="css/leaflet.awesome-markers.css">
````
````xml
<script src="js/leaflet.awesome-markers.js"></script>
````

- 3) Now use the plugin to create a marker like this:
````js
  // Creates a red marker with the coffee icon
  var redMarker = L.AwesomeMarkers.icon({
    icon: 'coffee',
    markerColor: 'red'
  });
      
  L.marker([51.941196,4.512291], {icon: redMarker}).addTo(map);
````

### Properties

| Property        | Description            | Default Value | Possible  values                                     |
| --------------- | ---------------------- | ------------- | ---------------------------------------------------- |
| icon            | Name of the icon       | 'home'        | See glyphicons or font-awesome                       |
| prefix          | Select de icon library | 'glyphicon'   | 'fa' for font-awesome or 'glyphicon' for bootstrap 3 |
| markerColor     | Color of the marker    | 'blue'        | 'white', 'red','darkred', 'lightred', 'orange', 'beige', 'green', 'darkgreen', 'lightgreen', 'blue', 'darkblue', 'lightblue', 'purple', 'darkpurple', 'pink', 'cadetblue', 'white', 'gray', 'lightgray', 'black' |
| iconColor       | Color of the icon      | 'white'       | 'white', 'black' or css code (hex, rgba etc) |
| spin            | Make the icon spin     | false         | true or false. Font-awesome required | 
| extraClasses    | Additional classes in the created <i> tag | '' | 'fa-rotate90 myclass' eller other custom configuration |


### Supported icons
The 'icon' property supports these strings:
- 'home'
- 'glass'
- 'flag'
- 'star'
- 'bookmark'
- .... and many more, see: http://fortawesome.github.io/Font-Awesome/icons/
- Or: http://getbootstrap.com/components/#glyphicons
- Or: http://ionicons.com

### Tips & Tricks

Tweak size and positioning of the icons:

````css
    .awesome-marker i {
        font-size: 18px;
        margin-top: 8px;
    }
````

Set default prefix to something other than `glypicon`

````js
    L.AwesomeMarkers.Icon.prototype.options.prefix = 'ion';
````

See [JSFIddle](http://jsfiddle.net/markmarijnissen/VPzu4/286/)

### Using Square Markers

![Square Markers screenshot](/screenshots/screenshot-square-markers.png "Screenshot of Square Markers")

````js
  // Creates a red square marker with the coffee icon
  var squareRedMarker = L.AwesomeMarkers.icon({
    icon: 'coffee',
    markerColor: 'red'
    className: 'awesome-marker awesome-marker-square'
  });
````

**note: square markers are only available on the latest versions of Leaflet.Awesome-Markers**

## License
- Leaflet.AwesomeMarkers and colored markers are licensed under the MIT License - http://opensource.org/licenses/mit-license.html.
- Font Awesome: http://fortawesome.github.io/Font-Awesome/license/
- Twitter Bootstrap: http://getbootstrap.com/

## Contact
- Email: atendimento@sigmageosistemas.com.br
- Website: http://www.sigmageosistemas.com.br
