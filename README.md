# jQuery.Readonly Plugin

## Info and Links

* Author: Me :p
* Compatibility: jQuery 1.6+ and most modern browsers
* License: Dual MIT / GPL
* [Bug Tracker](https://bugs.powelltechs.com/redmine/projects/jquery-readonly) (Registration is required)
* Demo (todo)

This plugin simply makes virtually any element on a page "readonly".  This includes input boxes, select boxes, radio options, anchors, paragraphs, divs, iframes, even the entire page.  I originally developed it for a select box since some browsers _(IE)_, don't support readonly as a valid attribute on them.

## Usage

To use this plugin, add the following to the `<head>` section of your page after your jquery include.
This will include the necessary scripts and styles to use this plugin, (of course update the directory path if necessary).
	
	<html>
	<head>
		<script type="text/javascript" src="jquery.js"></script>
		<script type="text/javascript" src="jquery.readonly.min.js"></script>
		<link rel="stylesheet" href="jquery.readonly.css" type="text/css">
	</head>
	<body>
		<input class="nointeraction" value="foo"/>
		<script type="text/javascript">
			$(function(){
				$('.nointeraction').readonly();
			});
		</script>
	</body>
	</html>


## Methods

	.readonly(true);

Enable an overlay on a target.

	.readonly(false);

Disable an existing overlay on a target.

	.readonly('destroy');

Disable and completely remove bindings on a target.


## Options 
_(usable during initial instantiation only)_

	"intervaltime"

milliseconds between each "tick".  If your application never moves elements, feel free to set this to really high.
Default: 250

	"overlayClass"

Default class to assign to the overlay.
Default: 'readonly_overlay'

	"title"

Text to place on the mouseover title for the overlay.
Default: ''

	"zindex"

Z-Index to assign to the overlay, use "auto" for auto.
Default: 'auto'

	"formtargets"

Any element which can be targetted.
Default: 'input,select,textarea,button,a'

	"show"

Function that is called during the show procedure of the overlay, (enabling it)
Default: function(overlay){
	overlay.show();
}

	"hide"

Function that is called during the hide procedure of the overlay, (disabling it)
Default: function(overlay){
	overlay.hide();
}

	"tick"

Function that is called during the "tick" timer.
Default: function(overlay){
	return;
}
