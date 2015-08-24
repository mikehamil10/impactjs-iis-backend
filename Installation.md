To set-up the IIS back-end for ImpactJS:

  * Unpack the ImpactJS engine files to your IIS web directory (usualy c:\inetpub\wwwroot)

  * Copy the files in this package to the /lib/weltmeister/api folder of the ImpactJS installation

  * Make the following changes to /lib/weltmeister/api/web.config:
    * Set the "fileRoot" key to the path in your IIS installation where this instance of ImpactJS is located. If the installation is at the root of the IIS website, leave the value at its default: "/". If, for example, you have Impact installed in the /impact folder in your IIS root, just change the web.config key to read "/impact". Simple as that!

  * Make the following changes to /lib/weltmeister/config.js:
    * change the 'save' value in the 'api' section to: 'lib/weltmeister/api/save.aspx' (line 72)
    * change the 'browse' value in the 'api' section to: 'lib/weltmeister/api/browse.aspx' (line 73)
    * change the 'glob' value in the 'api' section to: 'lib/weltmeister/api/glob.aspx' (line 74)

  * Browse to /weltmeister.html in your website and ensure that everything loaded and no exceptions were thrown (check the JavaScript error console in your browser).

Once you follow these steps, you should be able to work with ImpactJS in IIS
just as you would if you were running Apache/PHP.