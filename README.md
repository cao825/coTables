# coTables jQuery plugin
coTables is a [jQuery](//jquery.com) plugin for HTML table sorting, filtering, .xlsx export, and more.  By simply adding the plugin to your project, you can easily turn a normal static table into an interactive data set for your users.


## Installation & Setup

To install, place the js and css files into the appropriate areas of your project.  Then, include those on any pages you wish to use coTables.

You may need to configure several settings to get coTables to work the way you would like (See: Configurations).  Two settings that typically need configured on initial setup are: 
* imgPath - The path to your coTable images folder (default: /css/coTableImg)
* exportIcon - Custom path to xlsx export icon (Not needed if you use Font Awesome)


## Guide

The most basic and simple usage of coTables is to simple call the jQuery function on your table object:

```js
$('#myTableId').coTable();
```

However, most setups or custom/advanced usage will require the passing of settings / options.  These settings are passed in the form of a JSON array.  For example, most sites will need to identify imgPath and exportIcon:

```js
$('#myTableId').coTable( {
  imgPath: "/Content/css/coTableImg/",
  exportIcon: "/Content/css/coTableImg/export.png"
} );
```

A playground with example source and options testing can be found at [CraigOley.com/Home/coTables](http://CraigOley.com/Home/coTables)

## Settings / Options / Customizations


## Support

Support is currently handled through github issue requests.


## License

coTables is release under the [MIT license](//tldrlegal.com/license/mit-license). You are free to use, modify and distribute this software, as long as the copyright header is left intact.
