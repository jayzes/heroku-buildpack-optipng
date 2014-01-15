Heroku Buildpack: Optipng
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [optipng](http://optipng.sourceforge.net/) in your application.  

It is designed to be used with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to combine it with the appropriate real buildpack for your app.

This is based on http://github.com/jayzes/heroku-buildpack-ffmpeg, which was in turn based on https://github.com/shunjikonishi/heroku-buildpack-ffmpeg

Usage
-----
Add a `.buildpacks` file to the root of your repo that contains this buildpack URL and your real buildpack URL:

    https://github.com/jayzes/heroku-buildpack-optipng
    https://github.com/heroku/heroku-buildpack-ruby

Then create an application using the multi buildpack:

    $ heroku create --buildpack https://github.com/ddollar/heroku-buildpack-multi

or configure an existing application:

    $ heroku config BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi

You can verify that everything is properly installed by running the following command:

    $ heroku run "optipng -v"

