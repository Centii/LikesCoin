LikesCoin integration/staging tree
================================

http://www.likescoin.com

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2011-2013 LiteCoin Developers
Copyright (c) 2013-2014 LikesCoin Developers

What is LikesCoin?
----------------

LikesCoin is a version of Litecoin using scrypt as a proof-of-work algorithm.
 - 1 minute block targets
 - Flat reward system
 - 1,000,000,000,000 total coins to be mined
 - 1000 coins per block
 - 240 blocks to retarget difficulty

LikesCoin can be openly traded, or it's preferred use with the LikesCoin.com website. 


For more information, as well as an immediately useable, binary version of
the LikesCoin client sofware, see http://www.likescoin.com.

License
-------

LikesCoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the LikesCoin
development team members simply pulls it.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/deltajax/likescoin/tags) are created
regularly to indicate new official, stable release versions of LikesCoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./likescoin-qt_test

