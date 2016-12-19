# Social Buttons

**Installation**
```bash
npm install --save-dev social-sharing
```
**Usage**
**1.**
Add .css and .js files of socialSharing and its dependency, pureMasonry to your project code.
```html
<head>
	...
	<link rel="stylesheet" href="node_modules/pure-masonry/src/pureMasonry.min.css">
	<link rel="stylesheet" href="node_modules/social-sharing/src/socialSharing.min.css">
	...
</head>
<body>
	...
	<script type="text/javascript" src="node_modules/pure-masonry/src/pureMasonry.min.js"></script>
	<script type="text/javascript" src="node_modules/social-sharing/src/socialSharing.min.js"></script>
</body>
```
**2.**
Initialise app and pass a configuration object to it:
```javascript
socialButtons.init({
	distanceFromTop: 10,
	orientation: 'right',
	buttonSize: 4,
	buttonRoundness: 7,
	googleAPIKey: '',
	socials: {
		facebook: {
			enabled: true
		},
		twitter: {
			enabled: true,
			text: '',
			hashtag: '',
			screenName: ''
		},
		googleplus: {
			enabled: true,
			url: ''
		},
		pinterest: {
			enabled: true
		},
		linkedin: {
			enabled: true,
			url: ''
		}
	}
});
```

*Options:*
**distanceFromTop**: distance of button container from the browser top in vh (default: 15)
**orientation**: whether to stick container to the left or right edge of the screen (default: right)
**buttonMobileSize**: button size for small devices in px (default: 38)
**buttonDesktopSize**: button size for large devices in px (default: 56)
**buttonRoundness**: border-radius of buttons in px (default: 0)
**buttonGreyscale**: whether to turn buttons to greyscale (default: false)
**enabled**: whether to add button (default: true for facebook and twitter only)
If Twitter is enabled, **text** and **hashtag** are mandatory fields; if **screenName**: is not specified, the value of 'hashtag' is used as default. If **googleAPIKey** is provided, a shortened url is sent to Twitter.