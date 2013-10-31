ripple-lib-java
===============

Java version of ripple-lib (alpha work in progress)

Currently looking for java/android developers to help evolve this library/api.

Please open an issue with any questions/suggestions.

The goal for this is to be an implementation of ripple-types, binary
serialization, with a websocket library agnostic implementation of a client,
which will track changes to accounts balances/offers/trusts, that can be used as
the basis for various clients/wallets.

Current status:

  - Working implementation of sjcl.json aes/ccm for (wallet) blob decrytion
  - Working implementation of binary serialization
  - Crude implementation of a high level client
  - Api client choice of websocket transport
  - Test suite for core types
  - Signing / Verification
  - KeyPair creation
  - Android example
    - Using class loader patch to use predexe Bouncy Castle 1.4.9
      - MUCH faster builds, don't need to dex or merge each time
      - No need to fork a squishy/boingy castle and maintain two crypto providers
  - CLI example

TODO:
  - Publisher contexts
    - thread execution context
      - runOnUiThread 
    - easily unbind handlers in onDestroy/onSemanticallyEtc

  - Class path patcher for android needs testing on 2.x
  - Binary parsing
  - Documentation
  - General cleanup of code / api surface

Examples:

  See in examples/ folder
