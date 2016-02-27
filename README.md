ParkManager AppSectioning configurator
====================================

The AppSectioning configurator helps with separating your Symfony application
into multiple sections (eg. frontend and backend). Each with there own
configurable URI pattern.

But this library does more!

Say there are two sections:

* Frontend - host: example.com prefix: /
* Backend  - host: example.com prefix: backend/

Unless the 'backend' section is tried earlier the 'frontend' will always match!
To prevent this the path (regex) is configured to never match 'backend/'.
Only when both share the same host group and only there is an actual conflict.

You then use these generated parameters for routing and security firewalls.

And where there is a conflict, eg. both share the same hos and prefix you will be
informed about this error.

**Coming-up:** At this moment you can only use static values, but in the future
it will be possible to also use regexp and placeholders with conflict detection.

Park-Manager
------------

Park-Manager is your friend in hosting software. Visit [Park-Manager.com](http://www.park-manager.com)

Requirements
------------

You need at least PHP 7.0, the Symfony FrameworkBundle and Routing Component.

Installation
------------

To install this package, add `parkmanager/app-sectioning-bundle` to your composer.json

```bash
$ php composer.phar require parkmanager/app-sectioning-bundle
```

Now, Composer will automatically download all required files, and install them
for you.

Basic usage
-----------

TBD.

Versioning
----------

For transparency and insight into the release cycle, and for striving
to maintain backward compatibility, this package is maintained under
the Semantic Versioning guidelines as much as possible.

Releases will be numbered with the following format:

`<major>.<minor>.<patch>`

And constructed with the following guidelines:

* Breaking backward compatibility bumps the major (and resets the minor and patch)
* New additions without breaking backward compatibility bumps the minor (and resets the patch)
* Bug fixes and misc changes bumps the patch

For more information on SemVer, please visit <http://semver.org/>.

License
-------

The package is provided under the none-restrictive MIT license,
you are free to use it for any free or proprietary product/application,
without restrictions.

[LICENSE](LICENSE)