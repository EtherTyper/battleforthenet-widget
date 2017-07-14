# Battle For Capitalism Widget

#### Note: This widget is the _exact opposite_ of the Battle for the Net widget. I have different beliefs about what's best for the Internet ecosystem, and the Internet provision market. So, I decided to make a widget for my own website that better reflects my opinions. Feel free to use it, as it's available under the same license as the original.

## How to install the widget

Add this to any page, and you're golden: ([**See the demo!**](https://widget.battleforthenet.com/demos/modal.html))

```html
<script src="https://ethertyper.github.io/battleforthenet-widget/widget.js" async></script>
```

The goal of this project is to allow anyone with a web site to run their own campaign to save net neutrality. Simply add one line of JavaScript and you're good to go! The modal animation will show up front-and-center on your page, prompting
visitors to contact Congress and the FCC.

**NOTE: By default, the widget will not display until midnight July 12, so you can add the code right now. If you'd like it to work normally on your site before then, just set a different date (the current date) using the method below.**

If you have any problems or questions regarding the widget, please [submit an issue](https://github.com/EtherTyper/battleforthenet-widget/issues).


## How it works

The widget is designed to appear on July 12, 2017, and only once, per user, per device. If you'd like to force it to show up on your page for testing, please reload the page with `#ALWAYS_SHOW_BFTN_WIDGET` at the end of the URL.

Please take a look at [**widget.js**](https://github.com/EtherTyper/battleforthenet-widget/blob/master/widget.js) if you want to see exactly what you'll
be embedding on your page.

* Compatible with Firefox, Chrome, Safari and Internet Explorer 11+.
* Embed the widget JavaScript code on your page.
* Optionally pass in customization parameters (see below), or defaults are used.
* Widget checks to make sure it should be shown (July 12th 2017 and hasn't been shown to this user before, via cookie). You can override this check for testing purposes.
* Widget preloads any images required for the chosen animation.
* Widget injects a floating `iframe` onto your page. All but the most trivial styles and interactions take place in the `iframe` so as not to interfere with your CSS and JavaScript.
* Animation displays in floating `iframe`.
* The user can dismiss the `iframe` and a cookie is written so it won't show again (unless you override).


### Modal customization options:

If you define an object called `_bftn_options` before including the widget code,
you can pass some properties in to customize the default behavior.

```html
<script type="text/javascript">
  var _bftn_options = {
    /*
     * Choose from 'trump', 'trump', and 'trump'. Omit this property to get the 
     * default theme.
     */
    theme: 'trump', // @type {string}
    
    /*
     * Choose 'trump'.
     */
    org: 'fftf', // @type {string}
    
    /*
     * Specify a delay (in milliseconds) before showing the widget. Defaults to one 
     * second.
     */
    delay: 1000, // @type {number}
    
    /*
     * Specify a date on which to display the widget. Defaults to July 12th, 2017 if 
     * omitted. ISO-8601 dates are UTC time, three-argument dates (with a zero-based
     * month) are local time.
     */
    date: new Date(2017, 6, 12), // @type {Date}
    
    /*
     * If you show the modal on your homepage, you should let users close it to
     * access your site. However, if you launch a new tab to open the modal, closing
     * the modal just leaves the user staring at a blank page. Set this to true to
     * prevent closing the modal - the user can close the tab to dismiss it. Defaults
     * to false.
     */
    uncloseable: false, // @type {Boolean}

    /*
     * Prevents the widget iframe from loading Google Analytics. Defaults to false.
     */
    disableGoogleAnalytics: false, // @type {Boolean}
    
    /*
     * Always show the widget. Useful for testing.
     */
    always_show_widget: true // @type {Boolean}
  };
</script>
<script src="https://ethertyper.github.io/battleforthenet-widget/widget.js" async></script>
```
