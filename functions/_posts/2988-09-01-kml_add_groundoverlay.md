---
    layout: function
    title: kml_add_groundoverlay
    short: Adds a GroundOverlay element to a KML document.
    category: functions
    tags: overlay
    seealso: [ kml_plot_groundoverlay, kml_add_screenoverlay, kml_plot_screenoverlay ]
---

### Prototype

<pre><code>load "/usr/local/lib/ncarg/nclscripts/kml/kml.ncl"

function kml_add_groundoverlay (
  kml:string,
  name:string,
  icon:string,
  LatLonBox[4]:float,
  z[1]:float,
  res:logical
)

returnval [*]  :  string
</code></pre>

### Arguments
*kml*

A string array containing a KML document and associated attributes created with the function [kml_open_document]({{site.url}}/functions/kml_open_document.html).

*name*

Text string displayed in Google Earth (or other geobrowser) as the label for the GroundOverlay.

*icon*

An HTTP address or a local file specification used to load the GroundOverlay image.

*LatLonBox*

A vector containing the coordinates defining the top, bottom, right, and left corners of a bounding box for the ground overlay image.

*z*

Altitude at which to display the ground overlay image.

*res*

A variable containing an optional list of [KML resources]({{site.url}}/resources), attached as attributes. Set to True if you want the attached attributes to be applied, and False if you either don't have any resources to set, or you don't want the resources applied.

### Return value

A string array containing a KML document with a GroundOverlay element appended to the end.

### Description

For more information about the GroundOverlay element, see the [Google KML Reference](https://developers.google.com/kml/documentation/kmlreference#groundoverlay) page or the [OGC KML specification](http://www.opengeospatial.org/standards/kml/).

### See Also

{% for seealso in page.seealso %}
[{{seealso}}]({{site.url}}/functions/{{seealso}}.html)
{% endfor %}

### Examples

