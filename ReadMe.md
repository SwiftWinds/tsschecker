# tsschecker  
_tsschecker is a powerful tool to work with signing technology on iOS devices._

Latest compiled version can be found [here](https://github.com/s0uthwest/tsschecker/releases). Windows version is supported, but I will not compile it.

## Features  
* Allows you to get lists of all devices and all iOS/OTA versions for a specific device.
* Can check signing status for default iOS versions and beta iPSW's (by specifying a `BuildManifest.plist`)
* Works without specifying any device relevant values to check signing status, but can be used to save blobs when given an ECID and the option `--print-tss-response` (although there are better tools to do this).
* __If you want to save blobs with recommended ApNonce, please, see [this file](https://github.com/s0uthwest/tsschecker/blob/master/nonces.txt).__

tsschecker is not only meant to be used to check signing status, but also to explore Apple's TSS servers.
By using all of its customization possibilities, you might discover a combination of devices and iOS versions that is now getting signed but wasn't getting signed before.  

# Dependencies
*  ## Bundled Libs
  Those don't need to be installed manually
  * [tss](https://github.com/libimobiledevice)
* ## External Libs
  Make sure these are installed
  * [libcurl](https://curl.haxx.se/libcurl/)
  * [libplist](https://github.com/libimobiledevice/libplist)
  * [libfragmentzip](https://github.com/encounter/libfragmentzip)
  * [openssl](https://github.com/openssl/openssl) or commonCrypto on macOS/OS X.
  * [libirecovery](https://github.com/libimobiledevice/libirecovery)
* ## Submodules
  Make sure these projects compile on your system
  * [jssy](https://github.com/tihmstar/jssy)

## Compiling
Open terminal and execute the command: `./autogen.sh && make` or use Xcode project.

### Some about curl for ubuntu
Follow [this guide](https://dev.to/jake/using-libcurl3-and-libcurl4-on-ubuntu-1804-bionic-184g) to use tsschecker on Ubuntu 18.04 (Bionic) as it requires libcurl3 which cannot coexist with libcurl4 on this OS.

## Report an issue
You can do it [here](https://github.com/s0uthwest/tsschecker/issues).

## Credits
Creator of [original project](https://github.com/tihmstar/tsschecker) - [tihmstar](https://github.com/tihmstar).


ReadMe updated on:
     2019-01-08
