OpenEMR Module Composer Plugin installer that installs either Custom or Zend modules into the correct directory path using composer for an OpenEMR codebase.

Developers who wish to use composer to install their plugins can include in their composer.json the following composer types

For Custom Modules

```
/** composer.json ***/
{
    "name": "openemr/SomeCustomModule",
    "type": "openemr-zend-module",
    "require": {
        "adunsulag/openemr-module-installer-plugin": "*"
    },
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/adunsulag/openemr-module-installer-plugin"
        }
    ],
}
```
The above module will install in the *interface/modules/zend/modules/SomeCustomModule/* directory

For Zend Framework Modules

```
/** composer.json ***/
{
    "name": "openemr/SomeCustomModule",
    "type": "openemr-zend-module",
    "require": {
        "adunsulag/openemr-module-installer-plugin": "*"
    },
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/adunsulag/openemr-module-installer-plugin"
        }
    ],
}
```
The above module will install in the *interface/modules/custom_modules/SomeCustomModule/* directory
