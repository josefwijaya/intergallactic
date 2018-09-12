Intergallactic
==============

This is the main class of intergallactic library that act as a parent of all
modules that helps to interact with gallactic blockchain node.

To start using intergallactic to interract with the node, you need to instantiate
the `Intergallactic` object.

.. code-block:: javascript

  const Intergallactic = require('intergallactic');
  const intergallactic = new Intergallactic({ 'http://localhost:1337', protocol: 'jsonrpc' });

Upon instantiating Intergallactic, it will return main modules to interract
with gallactic blockchain node such as following:

- account
- gltc
- Txn
- Contract
- utils

account
-------