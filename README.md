
Thenable
========

Embeddable Minimum Strictly-Compliant Promises/A+ 1.1.1 Thenable<br/>
Copyright (c) 2013-2014 Ralf S. Engelschall (http://engelschall.com)<br/>
Licensed under The MIT License (http://opensource.org/licenses/MIT)

Abstract
--------

This is a strictly-compliant [Promises/A+](http://promisesaplus.com/)
1.1.1 implementation, which passes the [official Promises/A+
Test-Suite](https://github.com/promises-aplus/promises-tests). It just
provides a minimum Promise functionality, because it is intended to be
directly *embedded* into ECMAScript 5 based libraries and frameworks, in
order to dependency-free leverage from Promises and be able to return
"thenable" Promise objects to applications. As such, it only provides
the bare Promise creation and resolving functionalities and no general Promise
management functionalities. For applications (and similar contexts where
extra dependencies do not matter), please use a full-featured
Promise library like [Bluebird](https://github.com/petkaantonov/bluebird) instead.

Usage
-----

As Thenable is intended for embedding into dependency-free libraries and
frameworks, it is neither published to the Node NPM registry
nor to the Bower registry. Instead, please download the
raw [thenable.min.js](https://raw.githubusercontent.com/rse/thenable/master/thenable.min.js)
and include it verbatim into your library/framework.
Inside your library/framework use `var Promise = Thenable.noConflict()`
to retrieve the code without polluting the global namespace.

Features
--------

- strictly-compliant to Promises/A+ 1.1.1
- bare Promise creation and resolving functionality
- Universal Module Definition (UMD) for AMD, CommonJS and Browser support
- optional `noConflict` method for non-invasive use in Browser environments
- Static Constructor Function support
- additional Promise Proxy support
- additional Constructor Executor support
- permissive MIT license

