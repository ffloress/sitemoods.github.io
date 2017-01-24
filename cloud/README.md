s3commander
===========

Web-based S3 file browser.

Requirements
------------

* Bootstrap 3.0.0+
* jQuery 1.11.2+

Quick Setup
-----------

Include the necessary scripts and stylesheets.

```html
<link rel="stylesheet" href="s3commander.css" />
<script src="sha1.js"></script>
<script src="s3commander.js"></script>
```

Create a ```<div />``` element to display the browser.

```html
<div id="s3commander"></div>
```

Initialize the browser.

```javascript
$(document).ready(function(){
    $("#s3commander").s3commander({
        sAccessKey: "...",
        sSecretKey: "...",
        sBucket: "bucketname",
        sPrefix: "/super/secure/stuff",
    });
})
```

Take a look at the included ```index.html``` file for a more complete example.

Quirks
------

* Folders are just S3 objects where the key ends in a trailing slash.
* Deleting a folder does not delete its contents. It will still appear in the
  browser as a folder until its contents are deleted.
* When not using Dropzone for drag-and-drop uploads, the directory contents will
  not automatically refresh after a file is uploaded. The user needs to click
  the refresh button manually.

Contributing
------------

See the [Contributing Guidelines](CONTRIBUTING.md).

Version History:
----------------

v0.3.10 - July 1, 2015

    * Adding cursor style to s3links.  Updated bootstrap from CDN in example index.html.

v0.3.9 - June 30, 2015

    * Added button for file uploads.  Made icons clickable.  Made files have 'click' pointer.

v0.3.8 - June 18, 2015

    * Fixed issue with losing versions.  Changed signing method to (properly) allow for spaces (and likely other escape-needing characters).

v0.3.7 - June 14, 2015

    * Implemented iMaxFilesize.  Set default to 1GB (10GB in example HTML).
