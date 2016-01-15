## jQuery Image Gallery Plugin 

## Instructions
Full instructions are contained in the html files. 

## Plugin options

When you apply the plugin to your images, you can provide settings to your liking.  
Example of applying Etalage with custom settings:  

    <script type="text/javascript">
    $(document).ready(function(){
    
    // If your <ul> has the id "etalage":
    $('#etalage').etalage({
    // These are the most common settings (because they are case specific)
    thumb_image_width: 300,
    thumb_image_height: 400,
    source_image_width: 1200,
    source_image_height: 1600,
    zoom_area_width: 800
    // Note: the last option does not end with a comma
    }); 
    
    });
    </script>

## Options List
<table class="list">

<tbody>

<tr>

<th>Name</th>

<th>Description</th>

<th>Default</th>

</tr>

<tr>

<td class="option">align</td>

<td>Align of the Etalage container. The zoom area will appear on the opposite side ('left'/'right')</td>

<td class="default">'left'</td>

</tr>

<tr>

<td class="option">thumb_image_width</td>

<td>The large thumbnail width (excluding borders / padding) (value in pixels)</td>

<td class="default">300</td>

</tr>

<tr>

<td class="option">thumb_image_height</td>

<td>The large thumbnail height (excluding borders / padding) (value in pixels)</td>

<td class="default">400</td>

</tr>

<tr>

<td class="option">source_image_width</td>

<td>The source/zoomed image width (not the frame around it) (value in pixels)</td>

<td class="default">900</td>

</tr>

<tr>

<td class="option">source_image_height</td>

<td>The source/zoomed image height (not the frame around it) (value in pixels)</td>

<td class="default">1200</td>

</tr>

<tr>

<td class="option">zoom_area_width</td>

<td>Width of the zoomed image frame (including borders, padding) (value in pixels)</td>

<td class="default">600</td>

</tr>

<tr>

<td class="option">zoom_area_height</td>

<td>Height of the zoomed image frame (including borders, padding)  
(value in pixels / 'justify' = automatic (height of large thumb + small thumbs))</td>

<td class="default">'justify'</td>

</tr>

<tr>

<td class="option">zoom_area_distance</td>

<td>Distance between the zoom area and thumbnail (value in pixels)</td>

<td class="default">10</td>

</tr>

<tr>

<td class="option">zoom_easing</td>

<td>Ease the animation while moving the zoomed image (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">click_to_zoom</td>

<td>Will start zooming when image is clicked instead of when hovering (when true, click-callback functions are disabled) (true/false)</td>

<td class="default">false</td>

</tr>

<tr>

<td class="option">zoom_element</td>

<td>Supply your custom zoom area element as a CSS type selector ('auto'/'#selector'/'.selector'). This allows for more freedom in positioning the zoom area outside of the Etalage container. To change the dimensions, set the "zoom_area_width" and "zoom_area_height" options to their pixel values.</td>

<td class="default">'auto'</td>

</tr>

<tr>

<td class="option">show_descriptions</td>

<td>Shows the description area if a title attribute is given to the source image (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">description_location</td>

<td>Location of the description area ('top'/'bottom')</td>

<td class="default">'bottom'</td>

</tr>

<tr>

<td class="option">description_opacity</td>

<td>Opacity of the description area (except for IE) (number between or equal to 0-1)</td>

<td class="default">0.7</td>

</tr>

<tr>

<td class="option">small_thumbs</td>

<td>How many small thumbnails will be visible underneath the large thumbnail  
(minimum of 3) (number)</td>

<td class="default">3</td>

</tr>

<tr>

<td class="option">smallthumb_inactive_opacity</td>

<td>Opacity of the inactive small thumbnails (number between or equal to 0-1)</td>

<td class="default">0.4</td>

</tr>

<tr>

<td class="option">smallthumb_hide_single</td>

<td>Don't show the small thumb when there is only 1 image (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">smallthumb_select_on_hover</td>

<td>This will scroll through the small thumbnails when hovering them, instead of clicking them (true/false)</td>

<td class="default">false</td>

</tr>

<tr>

<td class="option">smallthumbs_position</td>

<td>Where to position the row of small thumbnails ('top'/'bottom'/'left'/'right')</td>

<td class="default">'bottom'</td>

</tr>

<tr>

<td class="option">show_begin_end_smallthumb</td>

<td>Whether to show extra thumbnails at the beginning and the end that navigate back to the end or beginning (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">magnifier_opacity</td>

<td>Opacity of the magnifier area (does not apply if magnifier_invert is true)  
(number between or equal to 0-1)</td>

<td class="default">0.5</td>

</tr>

<tr>

<td class="option">magnifier_invert</td>

<td>Make the large thumbnail clear through the magnifier, opaque around it  
(opacity is the value of magnifier_opacity) (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">show_icon</td>

<td>Shows the icon image in the middle of the magnifier (only if magnifier_invert is false) and left-bottom of large thumb (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">icon_offset</td>

<td>The icon's offset to the left-bottom corner (value in pixels)</td>

<td class="default">20</td>

</tr>

<tr>

<td class="option">hide_cursor</td>

<td>Hides the cursor when hovering the large thumbnail  
(only works in some browsers) (true/false)</td>

<td class="default">false</td>

</tr>

<tr>

<td class="option">show_hint</td>

<td>Show "hint" until image is zoomed for the first time (true/false)</td>

<td class="default">false</td>

</tr>

<tr>

<td class="option">hint_offset</td>

<td>The hint's offset to the right-top corner (value in pixels)</td>

<td class="default">15</td>

</tr>

<tr>

<td class="option">speed</td>

<td>All animation speeds are based on this setting (value in ms)</td>

<td class="default">600</td>

</tr>

<tr>

<td class="option">autoplay</td>

<td>Makes the thumbs switch automatically when not interacting  
(at each autoplay_interval below) (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">autoplay_interval</td>

<td>Time showing each image if autoplay is on (value in ms)</td>

<td class="default">6000 (6 seconds)</td>

</tr>

<tr>

<td class="option">keyboard</td>

<td>Left/right arrow keys to navigate (true/false)</td>

<td class="default">true</td>

</tr>

<tr>

<td class="option">right_to_left</td>

<td>Makes the thumbnails slide from right to left and the caption texts RTL (true/false)</td>

<td class="default">false</td>

</tr>

<tr>

<td class="option">click_callback</td>

<td>Provide your own callback for the click event (function). Takes 2 arguments: image_anchor, instance_id. The old callback function method (up to v.1.3.1) is still supported in case you are already using those. Example:  

<pre>
    
    $('etalage').etalage({
    click_callback: function(image_anchor, instance_id){
    alert('Callback example:\nYou clicked on an image with the anchor: "'+image_anchor+'"\n(in Etalage instance: "'+instance_id+'")');
    }
    });
    
</pre>

</td>

<td class="default">function(){ return true; }</td>

</tr>

<tr>

<td class="option">change_callback</td>

<td>Provide your own callback for the change event (thumb switching) (function). Takes 2 arguments: image_number, instance_id. The old callback function method (up to v.1.3.1) is still supported in case you are already using those. Example:  

<pre>
    $('etalage').etalage({
    change_callback: function(image_number, instance_id){
    alert('Callback example: New active image: '+image_number+' (in Etalage instance: '+instance_id+')');
    }
    });
</pre>

</td>

<td class="default">function(){ return true; }</td>

</tr>

</tbody>

</table>

## HTML setup

Create a list of images in an Unordered List. One image as the source image, another as the thumbnail. The thumbnail will be a resized source image if not provided (not recommended for beauty and performance).  

    <!-- Give it any id or class to identify it with: -->
    <ul id="etalage">
    <li>
    <!-- This is the large (zoomed) image source: -->
    <img class="etalage_source_image" src="/images/large_image_1.jpg" title="Optionally, your description goes here." /> 
    
    <!-- This is the thumb image source (if not provided, it will use the large image source and resize it): -->
    <img class="etalage_thumb_image" src="/images/thumb_image_1.png" />
    </li>
    </ul>

