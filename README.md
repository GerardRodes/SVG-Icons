# SVG-Icons
###jQuery - SVG Social Networks Icons Generator

![SVG Icons](http://i.imgur.com/lCJzBTa.gif)  


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


##EXAMPLE OF USAGE
*This HTML*
```html
<ul data-social-links data-size="64" data-color="#333" data-shape="circle" data-hover="transform:scale(1.2)">
	<li data-social data-name="facebook" data-url="https://www.facebook.com" data-msg="I never use it, but you can follow me at "></li>
	<li data-social data-name="twitter" data-url="https://twitter.com"></li>
	<li data-social data-name="google" data-url="https://plus.google.com"></li>
	<li data-social data-name="skype" data-url="skype:YourSkypeName?call" data-transition="1s ease-out" data-hover="transform:rotate(360deg) scale(1.5) translate(25px,0)"></li>
</ul>
```
*Will become into this*
```html
<ul data-social-links="" data-size="64" data-color="#333" data-shape="circle" data-hover="transform:scale(1.2)" style="list-style: none; margin: 0px; transition: 0.35s;">
    <li data-social="" data-name="facebook" data-url="https://www.facebook.com" data-msg="I never use it, but you can follow me at " style="display: inline-block; margin: 0px; padding: 0px; transition: 0.35s;">
        <a href="https://www.facebook.com" title="I never use it, but you can follow me at Facebook" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="social-link-facebook-0" x="0px" y="0px" width="64" height="64" viewBox="0 0 56.693 56.693" enable-background="new 0 0 56.693 56.693" xml:space="preserve" fill="#333" style="transition: 0.35s;">
                <path d="M28.347,5.157c-13.6,0-24.625,11.027-24.625,24.625c0,13.6,11.025,24.623,24.625,24.623c13.6,0,24.625-11.023,24.625-24.623  C52.972,16.184,41.946,5.157,28.347,5.157z M34.864,29.679h-4.264c0,6.814,0,15.207,0,15.207h-6.32c0,0,0-8.307,0-15.207h-3.006  V24.31h3.006v-3.479c0-2.49,1.182-6.377,6.379-6.377l4.68,0.018v5.215c0,0-2.846,0-3.398,0c-0.555,0-1.34,0.277-1.34,1.461v3.163  h4.818L34.864,29.679z"></path>
            </svg>
        </a>
    </li>
    <li data-social="" data-name="twitter" data-url="https://twitter.com" style="display: inline-block; margin: 0px; padding: 0px; transition: 0.35s;">
        <a href="https://twitter.com" title="Contact on Twitter" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="social-link-twitter-1" x="0px" y="0px" width="64" height="64" viewBox="0 0 56.693 56.693" enable-background="new 0 0 56.693 56.693" xml:space="preserve" fill="#333" style="transition: 0.35s;">
                <path d="M28.348,5.157c-13.6,0-24.625,11.027-24.625,24.625c0,13.6,11.025,24.623,24.625,24.623c13.6,0,24.623-11.023,24.623-24.623  C52.971,16.184,41.947,5.157,28.348,5.157z M40.752,24.817c0.013,0.266,0.018,0.533,0.018,0.803c0,8.201-6.242,17.656-17.656,17.656  c-3.504,0-6.767-1.027-9.513-2.787c0.486,0.057,0.979,0.086,1.48,0.086c2.908,0,5.584-0.992,7.707-2.656  c-2.715-0.051-5.006-1.846-5.796-4.311c0.378,0.074,0.767,0.111,1.167,0.111c0.566,0,1.114-0.074,1.635-0.217  c-2.84-0.57-4.979-3.08-4.979-6.084c0-0.027,0-0.053,0.001-0.08c0.836,0.465,1.793,0.744,2.811,0.777  c-1.666-1.115-2.761-3.012-2.761-5.166c0-1.137,0.306-2.204,0.84-3.12c3.061,3.754,7.634,6.225,12.792,6.483  c-0.106-0.453-0.161-0.928-0.161-1.414c0-3.426,2.778-6.205,6.206-6.205c1.785,0,3.397,0.754,4.529,1.959  c1.414-0.277,2.742-0.795,3.941-1.506c-0.465,1.45-1.448,2.666-2.73,3.433c1.257-0.15,2.453-0.484,3.565-0.977  C43.018,22.849,41.965,23.942,40.752,24.817z"></path>
            </svg>
        </a>
    </li>
    <li data-social="" data-name="google" data-url="https://plus.google.com" style="display: inline-block; margin: 0px; padding: 0px; transition: 0.35s;">
        <a href="https://plus.google.com" title="Contact on Google" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="social-link-google-2" x="0px" y="0px" width="64" height="64" viewBox="0 0 56.6934 56.6934" style="transition: 0.35s;" xml:space="preserve" fill="#333">
                <path d="M28.4597,4.0154c-13.6006,0-24.625,11.0273-24.625,24.625c0,13.5996,11.0244,24.623,24.625,24.623  c13.5996,0,24.625-11.0234,24.625-24.623C53.0847,15.0426,42.0593,4.0154,28.4597,4.0154z M42.6077,33.8793  c-0.6971,2.4016-2.0137,4.6364-3.8595,6.3326c-1.7462,1.6122-3.9333,2.7168-6.2449,3.2488  c-2.5577,0.5821-5.2626,0.5976-7.8036-0.084c-2.0137-0.5356-3.9131-1.4954-5.5425-2.7948  c-1.7272-1.3727-3.1511-3.1237-4.1442-5.0933c-1.5282-3.0176-1.9982-6.5501-1.3239-9.8632  c0.2681-1.3298,0.7144-2.6226,1.3256-3.8339c1.7558-3.5151,4.9224-6.2962,8.6412-7.5694c3.3-1.1421,6.9968-1.1165,10.2748,0.09  c1.8207,0.6685,3.4871,1.726,4.9086,3.0414c-0.4755,0.5165-0.9914,0.9974-1.4823,1.5002c-0.936,0.9342-1.869,1.8719-2.8068,2.8043  c-0.9276-0.8859-2.0602-1.5591-3.2887-1.9321c-1.4454-0.4373-3.0021-0.4975-4.4785-0.1823  c-1.7242,0.3694-3.3245,1.2702-4.5554,2.5303c-0.9979,1.0104-1.7576,2.252-2.2139,3.5961c-0.6577,1.9071-0.653,4.0311-0.003,5.9399  c0.6357,1.8767,1.8737,3.5443,3.496,4.684c1.0146,0.7155,2.1776,1.2231,3.396,1.4662c1.1981,0.2425,2.4391,0.2163,3.6402,0.0114  c1.1934-0.2091,2.351-0.6488,3.3584-1.3262c1.6027-1.0706,2.7328-2.8097,3.054-4.7114c-2.7704-0.0012-5.5414-0.0006-8.3124,0  c-0.0035-1.9839-0.0005-3.9685-0.0012-5.953c4.7847-0.0006,9.5694-0.0018,14.3541,0.0005  C43.4728,28.4631,43.3679,31.2596,42.6077,33.8793z"></path>
            </svg>
        </a>
    </li>
    <li data-social="" data-name="skype" data-url="skype:YourSkypeName?call" data-hover="transform:rotate(360deg) scale(1.5) translate(25px,0);transition: 1s ease-out" style="display: inline-block; margin: 0px; padding: 0px; transition: 0.35s;">
        <a href="skype:YourSkypeName?call" title="Contact on Skype" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="social-link-skype-3" x="0px" y="0px" width="64" height="64" viewBox="0 0 56.693 56.693" enable-background="new 0 0 56.693 56.693" xml:space="preserve" fill="#333" style="transition: 1s ease-out;">
                <g>
                    <path d="M33.977,29.739c-0.658-0.43-1.469-0.799-2.404-1.098c-0.926-0.297-1.971-0.572-3.109-0.814   c-0.898-0.209-1.555-0.369-1.945-0.477c-0.383-0.105-0.764-0.254-1.133-0.441c-0.355-0.178-0.639-0.391-0.838-0.637   c-0.189-0.23-0.281-0.498-0.281-0.818c0-0.52,0.285-0.963,0.873-1.348c0.607-0.398,1.428-0.602,2.436-0.602   c1.086,0,1.875,0.184,2.35,0.545c0.484,0.369,0.91,0.895,1.262,1.561c0.303,0.52,0.574,0.885,0.838,1.115   c0.283,0.252,0.691,0.379,1.211,0.379c0.574,0,1.061-0.203,1.445-0.604c0.383-0.396,0.576-0.854,0.576-1.357   c0-0.521-0.148-1.062-0.439-1.604c-0.289-0.539-0.75-1.055-1.367-1.537c-0.613-0.481-1.396-0.87-2.322-1.161   c-0.922-0.285-2.025-0.432-3.283-0.432c-1.57,0-2.959,0.221-4.125,0.652c-1.184,0.438-2.102,1.075-2.73,1.895   c-0.633,0.826-0.955,1.783-0.955,2.846c0,1.115,0.306,2.062,0.912,2.82c0.594,0.742,1.406,1.336,2.414,1.766   c0.986,0.42,2.227,0.789,3.686,1.104c1.074,0.225,1.941,0.439,2.58,0.639c0.613,0.191,1.119,0.471,1.5,0.828   c0.365,0.342,0.545,0.779,0.545,1.334c0,0.703-0.34,1.275-1.041,1.754c-0.717,0.49-1.67,0.738-2.834,0.738   c-0.844,0-1.533-0.123-2.043-0.363c-0.506-0.24-0.902-0.547-1.178-0.914c-0.287-0.379-0.559-0.859-0.809-1.43   c-0.223-0.523-0.5-0.932-0.824-1.205c-0.338-0.287-0.756-0.432-1.238-0.432c-0.59,0-1.082,0.184-1.469,0.547   c-0.389,0.363-0.586,0.812-0.586,1.328c0,0.822,0.304,1.68,0.9,2.539c0.592,0.854,1.37,1.545,2.315,2.055   c1.322,0.701,3.016,1.059,5.035,1.059c1.684,0,3.162-0.262,4.395-0.773c1.246-0.52,2.207-1.248,2.857-2.166   c0.654-0.928,0.984-1.982,0.984-3.141c0-0.967-0.191-1.801-0.572-2.477C35.184,30.741,34.65,30.177,33.977,29.739z"></path>
                    <path d="M28.346,5.157c-13.599,0-24.624,11.027-24.624,24.625c0,13.6,11.024,24.623,24.624,24.623   c13.602,0,24.625-11.023,24.625-24.623C52.971,16.184,41.947,5.157,28.346,5.157z M34.367,45.104c-1.393,0-2.707-0.352-3.854-0.969   c-0.836,0.152-1.695,0.234-2.574,0.234c-7.768,0-14.064-6.297-14.064-14.062c0-0.969,0.097-1.914,0.284-2.828   c-0.711-1.211-1.121-2.619-1.121-4.125c0-4.504,3.65-8.157,8.155-8.157c1.598,0,3.082,0.461,4.34,1.254   c0.781-0.137,1.586-0.207,2.406-0.207c7.766,0,14.062,6.297,14.062,14.063c0,1.035-0.113,2.045-0.326,3.018   c0.543,1.092,0.85,2.32,0.85,3.623C42.525,41.452,38.873,45.104,34.367,45.104z"></path>
                </g>
            </svg>
        </a>
    </li>
</ul>
```
*And you will see this*  
![SVG Icons](http://i.imgur.com/lCJzBTa.gif)
