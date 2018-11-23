===============
Getting Started
===============

Intergallactic contains collections of modules with each does specific functionality
in gallactic ecosystem.

- ``Intergallactic.account``
- ``Intergallactic.gltc``
- ``Intergallactic.Txn``
- ``Intergallactic.Contract``
- ``Intergallactic.utils``


Importing Intergallactic
========================

To import intergallactic in your project, first you need to get it installed by
using following methods:

- npm: ``npm install intergallactic``

After the installation done, you need to create Intergallactic instance. To instantiate
intergallactic, you will need a local or remote gallactic node.

.. code-block:: javascript

  // in node.js
  const Intergallactic = require('intergallactic');
  const intergallactic = new Intergallactic({ url: 'http://localhost:1337/rpc', protocol: 'jsonrpc' });

  // in browser using pure javascript
  const intergallactic = new Intergallactic({ url: 'http://localhost:1337/rpc', protocol: 'jsonrpc' });

That's it! now you can use the ``intergallactic`` object.
