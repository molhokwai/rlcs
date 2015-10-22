_Name changed to Life Community Software, LCS_

## Purpose ##
Community network is meant for one purpose only: To connect people who want to start a real physical community together:

## Description ##
  * User's account is deleted after 6 months: user gets all of his data, and account is deleted. Real life takes over from there
  * Action & Events based: Which means there is room only for actions & events.

## Details ##
  * Built on & with Web2Py
  * Running on Web2Py, on [Google App Engine](GoogleAppEngine.md)

## Testing ##
Here: [staging](http://11.latest.molhokwai-net.appspot.com/lcs).
And there's a [simple test plan](Testing.md) available...

## Installing ##
You need:
  * [python2.5](http://www.python.org/download/releases/2.5/)
  * [web2py](http://www.web2py.com)
  * [Google App Engine](GoogleAppEngine.md)
  * [filestore application](http://code.google.com/p/rlcs/downloads/detail?name=filestore.mini-app.zip): google app engine app where all media files are stored
  * [web2py.app.lcs.w2p](http://code.google.com/p/rlcs/downloads/detail?name=web2py.app.lcs.w2p): the main app

Once web2py and google app engine are installed and running:
  * Add the web2py.app.lcs.w2p application through web2py's admin interface
    * In the <u>/admin/default/site</u> page choose <u>Upload & Install packed application</u>
    * Set configuration
      * Session sharing: remove session sharing, in `models/_db.py`, remove the `masterapp` optional parameter
      * Open Auth: obtain an api key for your domain from [RPX / Janrain](http://rpxnow.com) and set the `domain` and `api_key` values in the OAuth section in `models/_db.py`
    * and test it (<u>/lcs</u> or the name that you entered)
  * Add the filestore-mini.app application to google app engine: on port 8082 (the port that the main app expects)

To test the install, you can follow the [simple test plan](Testing.md) up to point 5.<u>View community</u>.

Voilà.

## Links ##
  * Under Construction prototype visible here: http://11.latest.molhokwai-net.appspot.com/lcs