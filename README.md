# jAlert

GitHub Project Link : http://cyberzilla.github.io/jAlert


I am not the author of this plugin. I just found it somewhere and thought it can be helpful for people like me!

This is just an fork of the work from (http://rajkumarpb.github.io/jAlert)
Since it isn't available in github and replaced with better one, I thought of put it here.

Original Source From http://labs.abeautifulsite.net/archived/jquery-alerts/



Demo Page
======
http://cyberzilla.github.io/jAlert/demo.html



Setup
======

Include the CSS/JS files somewhere in the page
```html
<!-- Dependencies -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.0.0-beta1/jquery.min.js" type="text/javascript"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" type="text/javascript"></script>
<script src="http://cdn.jsdelivr.net/jquery.validation/1.16.0/jquery.validate.js" type="text/javascript"></script>

<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet" type="text/css" media="screen" />
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" type="text/css" media="screen" />
<!-- Core files -->

<script src="jquery.alerts.js" type="text/javascript"></script>
<link href="jquery.alerts.css" rel="stylesheet" type="text/css" media="screen" />
```

Quick Use 
==========
```js
jAlert('This is a custom alert box', 'Alert Dialog');

jConfirm('Can you confirm this?', 'Confirmation Dialog', function(r) {
    jAlert('Confirmed: ' + r, 'Confirmation Results');
});

jPrompt('Type something:', 'Prefilled value', 'Prompt Dialog', function(r) {
    if( r ) alert('You entered ' + r);
});

//Use HTML in messages!
jAlert('You can use HTML, such as <strong>bold</strong>, <em>italics</em>, and <u>underline</u>!');

// To have custom button names in confirm other than Ok/Cancel
jCustomConfirm('Can you confirm this custom dialog?', 'Confirm Header', 'Think about it', 'Maybe Later');

// To have custom Popup with Form (Form Validation Support)
var template = '<form id="frmLogin" name="frmLogin" role="form">\
				<div class="form-group">\
					<div class = "input-group">\
						<input class="form-control input-sm" placeholder="Username" required type="text" data-msg="Username Required" name="Username">\
						<span class = "input-group-addon"><i class="fa fa-github"></i></span>\
					</div>\
				</div>\
				<div class="form-group">\
					<div class = "input-group">\
						<input class="form-control input-sm" placeholder="Email" required type="email" data-msg="Email Required" name="Email" data-msg-email="Wrong Email Format">\
						<span class = "input-group-addon"><i class="fa fa-envelope"></i></span>\
					</div>\
				</div>\
				</form>';
jCustomPopup(template, 'Form Login', 'Login', 'Cancel',function(r,data){
    //r    = return true if okButton Pressed
    //data = serialize value from defined form
	console.log(data);
});
```

You can even change the style dynamically. Just check out the demo page! This jAlert might not win beauty contest, but this is lot easier to use, looks like browser alert and smaller in size(~6KB js & css files combined)! Contributors are welcome!


in any html inside document.ready.

**Additional Information** : It supports IE7 and above! Yay! So for anyone out there who want an simple jquery alert plugin, this is it for you! Never tested in IE6, but as per the original author, it should work in IE6 too!


License 
=========
This plugin is dual-licensed under the GNU General Public License and the MIT License and is copyright 2008 A Beautiful Site, LLC.

