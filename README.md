# PopupMessage
Function-Based JavaScript/jQuery Object to build custom popup messages.

###Options:
 - title
 - message
 - button
 - cookie
 - cookieName
 - customCss
 - url

###Features:
 - optional 12hr or 1yr cookie
 - alternative to js alert() or other more complex (high overhead) js solutions
 - multi-instance
 - content manually or dynamically loaded

###Requires:
* jquery-1.11.1.min.js
* jquery.cookie.js

###Basic usage
```
   var message = new PopupMessage();
   message.init({
      title: 'string',       // required
      message: 'string',     // required, can be any valid html uses $.parseHTML()
      button: 'string'       // required, text used on the (dismissal) button
   });
```

###Usage with cookies and custom css class
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

###Usage with ajax
```
   $("{initializing_selector}").click(function(){
      var popUpSettings = {
         title:'Hello',
         message: '', //empty message here wont throw an error since the content will be fetched with ajax
         button: 'Dismiss',
         customCss: 'newName',
         url: 'path/to/content';,
      };
      loadRemotePopupContent(popUpSettings);
   });
```









