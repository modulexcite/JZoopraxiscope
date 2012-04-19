JZoopraxiscope
==============
**Animate static image sequenses with this jQuery plugin.**

JZoopraxiscope is a jQuery plugin for animations from static images. It is inspired in Eadweard Muybridge's Zoopraxiscope. 


Requierements
-------------
* JQuery
* JQuery UI
* An image representing the sequese to be animated


Use
---

1. Download JZoopraxiscope and link the jquery.jzoopraxiscope.js file in your page:

.. code:: html
		<script src="jquery.jzoopraxiscope.js"></script>


2. Link the jQuery and jQuery UI libraries in your page:
.. code:: html
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
		<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.18/jquery-ui.js"></script>
		
3. Prepare the static sequense. Every frame must have the same width and be attached to his previous frame in a horizontal image. Refer to the included file 'media/jzoo.jpg'

----------+------------+------------+------------+
|  Frame 1   |  Frame 2   |  Frame 3   |  Frame 4   |
+------------+------------+------------+------------+

*Horizontal image*


4. Define the options 

.. code:: javascript
			var optionsAnimation = {
				'widthItem' : 380,
				'widthImage' : 4560,
				'height' : 306,
				'image' : 'images/jzoo.jpg'
			}

widthItem
	Width of every frame.
widthImage
	Width of the entire image.
height
	Height of the image.
image
	Location of the image. Use relative or absolute path, relative paths are related to the html document where the plugin is installed.


5. Initialize a div with JZoo (#animation).

.. code:: html
		<div id="animation" style="border: 1px solid #999; margin: auto;"></div>

 
.. code:: javascript
		$('#animation').jzoopraxiscope(optionsAnimation);
				

6. Control JZoo.

.. code:: javascript
		//Play the animation
		$('#animation').jzoopraxiscope('play');
		
		//Stop the animation
		$('#animation').jzoopraxiscope('stop');