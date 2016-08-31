# SVG-Icons
###SVG Social Networks Icons Generator

Inserts svg icons to structures following this pattern
```
[data-social-links]			Wrapper attribute
	|->	[data-name]			Link element attribute, it can be anywhere inside the wrapper
```

Attributes placed at wrapper will be applied to all children link elements,
this attributes can be overwritted defining them at link element.
All attributes must be prefixed by `data-`, example: `data-color="black"`.
To disable an attributes just defined it with an invalid value, example: data-hover="none" (this would disable hover effects, however `data-hover=""` would be enough to disabled it)

##ATTRIBUTES  
```
color: 			CSS color string
shape: 			( normal | circle )
size:        	Size in px
hover: 			Hover css effectos to apply on hover => data-hover="attr1:value1;attr2:value2;attr3:value3..."
msg: 			Message before social network name at title attribue on link tag
transition: 	CSS transition to apply
target: 		target attribute value on link tag
folder: 		Url of the folder where the "svg" folder with the images is placed
css: 			Boolean, specifies if apply default css
```

##LINKS UNIQUE ATTRIBUTES  
```
url: 			Url to define href of the link tag
name: 			String to specify the social network, accepted values are store at `socialIcons` variable
```

Some CSS styles are applied to the wrapper and links by default, this styles are defined
on `css` variable. This can be disabled adding a value not `"true"` to the data-css tag.
This way you can disble css globally adding data-css="false" to the wrapper, and then
active css styles adding `data-css="true"` on some required elements.
