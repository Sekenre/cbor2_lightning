.. rst3: filename: SLIDES

####
CBOR
####

:Author: Kio Smallwood
:Date: 26/07/2019

Binary Serialization
++++++++++++++++++++

* Inspired by msgpack
* IETF proposed standard (RFC 7049)
* Tag-Length-Value encoding
* Designed to be compact
* Native recursive data structures
* Extensible tag system ( with an IANA registry )

    * e.g. Tag 258 encodes a Python Set

.. raw:: html

    <aside class="notes">
		inspired, meaning I didn't like the way you run your project so I'm going to fork it!
	</aside>

cbor2
+++++

https://github.com/agronholm/cbor2

* Pure Python implementation by Alex Grönholm
* Works in Python 2.7 to 3.6
* Clear and readable code
* Thorough test suite
* Only python cbor library that supports canonicalization

when to use?
++++++++++++

* When you need richer types than JSON or Msgpack
* When you don't want to write a schema
* When it needs to be more compact than XML

I use it for
++++++++++++

* Compacting time series data in CSV
* Internal APIs when I don't want to create a custom JSONEncoder just to send a datetime
* IoT messaging

The Future
++++++++++

* MicroPython?
* Nim?

Thanks!
+++++++

https://github.com/Sekenre

(If you need CBOR canonicalization come talk to me!)

