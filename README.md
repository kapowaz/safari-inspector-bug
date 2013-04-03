Safari Inspector Bug
====================

Simple demonstration test case for when the Safari web inspector fails to load (entirely blank, no DOM or resources visible). Reproducible under OS X 10.8.3 / Safari 6.0.3. Possibly introduced with 10.8.3…?

Steps to reproduce
------------------

Load index.html via an HTTP server; the bug isn't manifest when loading the page from the local filesystem. Try inspecting. Can't. 

(╯°□°）╯︵ ┻━┻

Cause
-----

The bug seems to be triggered by supplying multiple background images to an element, of which the last is a `-webkit-linear-gradient`. Reversing the order so that the `-webkit-linear-gradient` is first doesn't trigger the bug (but obviously has a different appearance).