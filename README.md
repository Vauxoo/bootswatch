Bootswatch
==========

Bootswatch is a collection of free themes for [Bootstrap](http://getbootstrap.com/). Check it out at [bootswatch.com](http://bootswatch.com).

Usage
-----
Download the `bootstrap.min.css` file associated with a theme and replace Bootstrap's default stylesheet.

The themes are also hosted on [BootstrapCDN](http://www.bootstrapcdn.com/).

Rails users should check out [twitter-bootswatch-rails](https://github.com/scottvrosenthal/twitter-bootswatch-rails).


Customization
------
Bootswatch is open source and you’re welcome to modify the themes.

Each theme consists of two LESS files. `variables.less`, which is included by default in Bootstrap, allows you to customize [these settings](http://getbootstrap.com/customize/#less-variables). `bootswatch.less` introduces more extensive structural changes.

Check out the [Help page](http://bootswatch.com/help/) for more details on building your own theme.

API
-----

A simple API is available for integrating your platform with Bootswatch. Send your request to `http://api.bootswatch.com/3/`.

The swatch objects are returned in an array called `themes`, each one with the following properties:  `name`, `description`, `preview`, `thumbnail`, `css`, `cssMin`, `less`, and `lessVariables`.

More info at http://bootswatch.com/help/#api

Author
------
Thomas Park

+ http://github.com/thomaspark
+ http://thomaspark.me

Thanks
------
[Mark Otto](http://github.com/markdotto) and [Jacob Thornton](http://github.com/fat) for [Bootstrap](https://github.com/twitter/bootstrap).

[Jenil Gogari](http://www.jgog.in/) for his contributions to the Flatly theme.

[James Taylor](http://github.com/jostylr) for [cors-lite](https://github.com/jostylr/cors-lite).


Copyright and License
----
Copyright 2014 Thomas Park

Code released under the MIT License.

How to create your own theme
----
To modify a theme or create your own, follow the steps below in your terminal. You'll need to have Git and Node installed.

`git clone https://github.com/thomaspark/bootswatch.git`
 
Then `cd` to bootswatch directory and run: 

`npm install`

Edit `variables.less` and `bootswatch.less` in one of the theme directories, or create your own in /custom.
If you want to create your own theme just copy a desired base theme ie. If you want to modify Yeti theme do `cp yeti your_own_theme_name`

Then edit the `index.html` of the root directory and add the path of your `your_own_theme_name` tho the list.

Install grunt `sudo npm install -g grunt-cli`.

After modifying the files as you want type `grunt swatch:your_own_theme_name` to build the CSS for a theme, e.g., grunt swatch:amelia for Amelia. Or type grunt swatch to build them all at once. To have grunt available in the command line, install grunt-cli as described on the Grunt Getting Started page.

