Heroku buildpack: Python, Brunch and Bower (node)
=================================================

This is a custom [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) likely of no interest to anyone outside of the project I'm currently working on.

It uses the standard Heroku python buildpack to install a Django application. It also, however, installs node and uses that to run both bower and brunch for building js/css.

Most of this buildpack's functionality could have been accomplished in a `bin/pre_compile` script except that the presence of a `package.json` file in the root of the application causes Heroku's build process to auto-detect a Node app rather than Python.

