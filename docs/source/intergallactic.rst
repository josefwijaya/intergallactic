==============
Intergallactic
==============

Upon instantiation of *Intergallactic*, it will returns an object

**Returns:**

``Object``: list of modules:

- ``Intergallactic.account``: Account related module. see :ref:`account <account>` for more.
- ``Intergallactic.gltc``: Gallactic blockhain related module. see :ref:`gallactic <gltc>` for more.
- ``Intergallactic.Txn``: Transaction related module. see :ref:`transaction <txn>` for more.
- ``Intergallactic.Contract``: Contract related module. see :ref:`contract <contract>` for more.
- ``Intergallactic.utils``: Utilities related module. see :ref:`utilities <utils>` for more.

**Example:**

.. code-block:: javascript

  // in node.js
  const Intergallactic = require('intergallactic');
  const intergallactic = new Intergallactic({ url: 'http://localhost:1337', protocol: 'jsonrpc' });

  // intergallactic consists of main modules to interact with Gallactic
  // e.g: intergallactic.account, intergallactic.gltc, intergallactic.Txn
