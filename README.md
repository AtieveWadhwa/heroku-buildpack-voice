# Heroku Buildpack - Voice

This is a simple Heroku Buildpack to setup a Nexmo Voice application. Purchase a new phone number and link that number to the application.


## Use
This buildpack is designed to be used in conjunction with an `app.json` manifest.<br>

The applicaiton will require 4 Environment Varibles to be setup (usually done in app.json)<br>

`API_KEY` - Your Nexmo API Key<br>
`API_SECRET` - Your Nexmo API Secret<br>
`CC` The ISO-3361-2 Country code where you want a number to be purchased<br>
`CREATE_NEXMO_APP` - Should be set to `yes` if you want an app and phone number to be created, set to no to skip the process, after the buildpack has run it will be set to done to prevent duplication.<br><br>


See the example `app.json` included in this repo to use as a base.<br><br>

Note that if you are including this buildpack then you need to also specify the buildpack which will run your code in the appropriate language as this will override herokus default detection. In the example "app.json" this is set to `heroku/python`<br><br>

https://devcenter.heroku.com/articles/buildpacks#officially-supported-buildpacks


