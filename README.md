Tamil and English: `apertium-tam-eng`
===============================================================================

This is an Apertium language pair for translating between Tamil and
English. What you can use this language package for:

* Translating between Tamil and English
* Morphological analysis of Tamil and English
* Part-of-speech tagging of Tamil and English

For information on the latter two points, see subheading "For more
information" below.

Requirements
-------------------------------------------------------------------------------

You will need the following software installed:

* lttoolbox (>= 3.3.0)
* apertium (>= 3.3.0)
* vislcg3 (>= 0.9.9.10297)
* hfst (>= 3.8.2)
* apertium-tam
* apertium-eng

If this does not make any sense, we recommend you look at: www.apertium.org.

Compiling
-------------------------------------------------------------------------------

Given the requirements being installed, you should be able to just run:

```console
$ ./configure
$ make
# make install
```

You can use `./autogen.sh` instead of `./configure` in case you're compiling
from source. If you installed any prerequisite language packages using a
`--prefix` with `./configure`, make sure to use the same `--prefix` when running
`./configure` here.

Testing
-------------------------------------------------------------------------------

If you are in the source directory after running make, the following
commands should work:

```console
$ echo "TODO test sentence 1" | apertium -d . tam-eng
TODO test translated sentence 1

$ echo "TODO test sentence 2" | apertium -d . eng-tam
TODO test translated sentence 2
```

After installing somewhere in `$PATH`, you should be able to do e.g.

```console
$ echo "TODO test sentence 1" | apertium tam-eng
TODO test translated sentence 1
```

Files and data
-------------------------------------------------------------------------------

* [`apertium-tam-eng.tam-eng.dix`](apertium-tam-eng.tam-eng.dix) - Bilingual dictionary
* [`apertium-tam-eng.tam-eng.t1x`](apertium-tam-eng.tam-eng.t1x) - Chunking rules for translating into English
* [`apertium-tam-eng.eng-tam.t1x`](apertium-tam-eng.eng-tam.t1x) - Chunking rules for translating into Tamil
* [`apertium-tam-eng.tam-eng.t2x`](apertium-tam-eng.tam-eng.t2x) - Interchunk rules for translating into English
* [`apertium-tam-eng.eng-tam.t2x`](apertium-tam-eng.eng-tam.t2x) - Interchunk rules for translating into Tamil
* [`apertium-tam-eng.tam-eng.t3x`](apertium-tam-eng.tam-eng.t3x) - Postchunk rules for translating into English
* [`apertium-tam-eng.eng-tam.t3x`](apertium-tam-eng.eng-tam.t3x) - Postchunk rules for translating into Tamil
* [`apertium-tam-eng.tam-eng.lrx`](apertium-tam-eng.tam-eng.lrx) - Lexical selection rules for translating into English
* [`apertium-tam-eng.eng-tam.lrx`](apertium-tam-eng.eng-tam.lrx) - Lexical selection rules for translating into Tamil
* [`modes.xml`](modes.xml) - Translation modes

For more information
-------------------------------------------------------------------------------

* http://wiki.apertium.org/wiki/Installation
* http://wiki.apertium.org/wiki/apertium-tam-eng
* http://wiki.apertium.org/wiki/Using_an_lttoolbox_dictionary

Help and support
-------------------------------------------------------------------------------

If you need help using this language pair or data, you can contact:

* Mailing list: apertium-stuff@lists.sourceforge.net
* IRC: `#apertium` on irc.freenode.net (irc://irc.freenode.net/#apertium)

See also the file [`AUTHORS`](AUTHORS), included in this distribution.
