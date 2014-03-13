Domecoin integration/staging tree
================================


Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2011-2013 Litecoin Developers
Copyright (c) 2014 Domecoin Developer

What is Domecoin?
----------------

Another scrypt coin. Well, gotta start somewhere, right?
Fork of the latest litecoin source.
Block reward - 718 per block for all 718 pokemon.
Halving time - Rewards halve every 700,000 blocks. 50% of the coins will be mined by the first halving, 75% by the second, 87.5% by the third, etc.
Block time - 30 seconds per block, just like the vote period of democracy mode.
Difficulty Adjustment - 30 blocks.
Premine - 5 million coins in Block 1. 0.05% of total, hopefully that won't upset many of you. This is almost 7000 blocks or about 2.5 days worth of mining.
Ports - RPC: 6886 P2P:6887 (Testnet - RPC: 16886 P2P:16887)

License
-------

Domecoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Domecoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Domecoin.

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

    qmake BITCOIN_QT_TEST=1 -o Makefile.test domecoin-qt.pro
    make -f Makefile.test
    ./domecoin-qt_test

