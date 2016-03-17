Heroku Buildpack: Optipng
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [optipng](http://optipng.sourceforge.net/) in your application.  

It is designed to be used with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to combine it with the appropriate real buildpack for your app.

This is based on http://github.com/jayzes/heroku-buildpack-ffmpeg, which was in turn based on https://github.com/shunjikonishi/heroku-buildpack-ffmpeg

Usage
-----
Add this buildpack to you existing app buildpacks:

    $ heroku buildpacks:add --index 1 https://github.com/jayzes/heroku-buildpack-optipng

Create a new release with a Git push. `heroku buildpacks:add` gives you the exact command line to do this, check its output.

You can verify that everything is properly installed by running the following command:

    $ heroku run "optipng -v"
