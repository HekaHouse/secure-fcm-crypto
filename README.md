# secure-fcm-crypto

`<secure-fcm-crypto>` A polymer element providing cloud messaging payload encryption.

[API Docs and Demo](https://heka-house-polymer-demos.firebaseapp.com/secure-fcm-crypto)

[Source](http://github.com/hekahouse/secure-fcm-crypto/)


## Install

    bower install --save HekaHouse/secure-fcm-crypto

## Example

    <secure-fcm-crypto
      poly-public-key="{{APP PUBLIC KEY}}"
      client-auth-secret="{{FCM AUTH SECRET}}"
      receiver-key="{{FCM P256 KEY}}"
      shared-secret="{{SHARED SECRET}}"></secure-fcm-crypto>

The following properties must be populated with base64 strings prior to calling encrypt:

polyPublicKey (created new for each message you encrypt)

clientAuthSecret (provided with service worker subscription to FCM/GCM)

receiverKey (provided with service worker subscription to FCM/GCM)

sharedSecret (derived from polyPublicKey and receiverKey used as basis for encryption key)

## Note

Process is based on [instructions from Google](https://developers.google.com/web/updates/2016/03/web-push-encryption?hl=en)

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

secure-fcm-crypto depends on

[secure-utils](http://github.com/hekahouse/secure-utils/)

includes embedded browser version of Buffer from Node.js

## Related

[secure-ecdh-secret](http://github.com/hekahouse/secure-ecdh-secret/)

[service-worker-subscription](http://github.com/hekahouse/service-worker-subscription/)
