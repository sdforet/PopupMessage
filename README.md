# PopupMessage
Function-Based JavaScript/jQuery Object to build custom popup messages, with optional 12hr/1yr cookie. Can be used as an alternate to js alert or other more complex (high overhead) js solutions.

###Include the following files in addition to this plugin:
* jquery-1.11.1.min.js
* jquery.cookie.js

###Sample usage within your js page's document.ready()
```
   var message = new PopupMessage();
   message.init({
      title: 'string',       // required
      message: 'string',     // required, can be any valid html uses $.parseHTML()
      button: 'string'       // required, text used on the (dismissal) button
      cookie: bool,          // optional, default=false
      cookieName: 'string',  // optional, default=popupMessage (use unique name in each multi-instance)
      customCss: 'string'    // optional, can add unique class name to each instance for custom css
   });
```
**Note:** when specifying `cookie:true`, the user will automatically get the option to "Dismiss Permanently" (aka 1yr cookie expiration).
