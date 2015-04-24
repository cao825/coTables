# coTables jQuery plugin
coTables is a [jQuery](//jquery.com) plugin for HTML table sorting, filtering, .xlsx export, and more.  By simply adding the plugin to your project, you can easily turn a normal static table into an interactive data set for your users.


## Installation & Setup

To install, place the js and css files into the appropriate areas of your project.  Then, include those on any pages you wish to use coTables.

You may need to configure several settings to get coTables to work the way you would like (See: Configurations).  Two settings that typically need configured on initial setup are: 
* imgPath - The path to your coTable images folder (default: /css/coTableImg)
* exportIcon - Custom path to xlsx export icon (Not needed if you use Font Awesome)


## External Package Notes

As this is a [jQuery](//jquery.com) plugin, it assumes you are already familiar with [jQuery](//jquery.com) and its use.

Web toolkits / plugins that are recommended to use with this plugin, but not included:
* [Font Awesome](//fortawesome.github.io/Font-Awesome/)
* [Bootstrap](//getbootstrap.com)

Javascript libraries also included in this plugin:
* [Blob.js](//github.com/eligrey/Blob.js/)
* [Filesaver.js](//github.com/eligrey/FileSaver.js/)
* [jszip.js](//stuk.github.io/jszip/)
* [xlsx.js](//github.com/SheetJS/js-xlsx)


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

Here are the current options available to customize the coTables plugin:
<table>
  <thead>
    <tr>
      <th>Setting</th>
      <th>Type</th>
      <th>Default</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>filterable</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Add filter boxes and hide non-matching filtered cells</td>
    </tr>
    <tr>
      <td>filterCaseSensitive</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Case sensitive matching for filters</td>
    </tr>
    <tr>
      <td>sortable</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Allow columns to be sorted</td>
    </tr>
    <tr>
      <td>exportable</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Allow table to be exported to .xlsx</td>
    </tr>
    <tr>
      <td>exportFileName</td>
      <td>String</td>
      <td>"coTableExport"</td>
      <td>Custom file name for .xlsx export</td>
    </tr>
    <tr>
      <td>exportIcon</td>
      <td>String</td>
      <td>""</td>
      <td>Image path to custom export icon - default adds Font Awesome Excel icon (http://fortawesome.github.io/Font-Awesome/icon/file-excel-o/)</td>
    </tr>
    <tr>
      <td>showTableInfo</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Display table information in a table header row.  Currently includes row count.</td>
    </tr>
    <tr>
      <td>alternateRows</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Alternate row colors.  Attempts to use  Bootstrap table stripe (http://getbootstrap.com/css/#tables-striped), but will pick up custom alternating row colors.</td>
    </tr>
    <tr>
      <td>highlightHoverRow</td>
      <td>Boolean</td>
      <td>true</td>
      <td>Highlight the row that the user is currently hovering their mouse over.  Attempts to use Bootstrap table hover (http://getbootstrap.com/css/#tables-hover-rows), but you can style table-hover:hover css however best fits your need.</td>
    </tr>
    <tr>
      <td>imgPath</td>
      <td>String</td>
      <td>"/css/coTableImg/"</td>
      <td>Path to the coTableImg directory where you are storing images for the coTable library</td>
    </tr>
  </tbody>
</table>


## Support & FAQ

HTML syntax note: Tables must be of the structure:
```
<TABLE>
  <THEAD>
    <TR>
      <TH>
      ...
      </TH>
    </TR>
  </THEAD>
  <TBODY>
    <TR>
      <TD>
      ...
      </TD>
    </TR>
  </TBODY>
</TABLE>
```

Support is currently handled through github issue requests.


## License

coTables is release under the [MIT license](//tldrlegal.com/license/mit-license). You are free to use, modify and distribute this software, as long as the copyright header is left intact.
