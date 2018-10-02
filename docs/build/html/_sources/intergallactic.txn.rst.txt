.. _txn:

===================
intergallactic.Txn
===================

Transaction related module are packed on this class. This allows user to be able
to initialize transaction according that suits Gallactic blockchain. Then upon
instantiation of this class, user able to sign, send and call the transaction.

*NOTE: Gallactic also supports performing bond, unbond and permission transaction, but
this features are still under developement till further notice*

signSync
========
Sign the transaction and return a signature that can be used for transaction.

**Returns:**

``String``: The signature string

**Example:**

.. code-block:: javascript

  const Transaction = intergallactic.Txn;
  const myTx = {
    from: [{
      address: 'acFbhUU8JK8mPhwYqMwy1DRrKP8fwUwnQMY',
      amount: 10,
      unit: 'boson'
    }],
    to: [{
      address: 'acQUFGxsXVPSd6vbAceSkURnWhYhApE9VRe',
      amount: 10
    }]
  };
  const opt = {
    type: Transaction.SEND_TYPE,
    chainId: 'test-chain-88291',
    sequence: 1
  };

  myTx = new Transaction(myTx, opt);
  myTx.signSync();
  // will return a string 'EB31F32425FA5FCB030B6FDF40B5A2F7598652AF897D64CA3A09121DBF0F59713FBEA213B0C9D5DCDB56746F2DF22EA4170451714CA3949F22BEBA7DB4C4F00C'


sign
=====
Sign the transaction and return a signature that can be used for transaction.

**Returns:**

``String``: The signature string

**Example:**

.. code-block:: javascript

  const Transaction = intergallactic.Txn;
  const myTx = {
    from: [{
      address: 'acFbhUU8JK8mPhwYqMwy1DRrKP8fwUwnQMY',
      amount: 10,
      unit: 'boson'
    }],
    to: [{
      address: 'acQUFGxsXVPSd6vbAceSkURnWhYhApE9VRe',
      amount: 10
    }]
  };
  const opt = {
    type: Transaction.SEND_TYPE
  };

  myTx = new Transaction(myTx, opt);
  myTx.sign()
    .then(signature => {
      // will return a string 'EB31F32425FA5FCB030B6FDF40B5A2F7598652AF897D64CA3A09121DBF0F59713FBEA213B0C9D5DCDB56746F2DF22EA4170451714CA3949F22BEBA7DB4C4F00C'
    });


broadcast
=========
Broadcast the transaction so the Gallactic blockchain can process the transaction.

**Returns:**

``Object``: Response object along with the transaction details

**Example:**

.. code-block:: javascript

  const Transaction = intergallactic.Txn;
  const myTx = {
    from: [{
      address: 'acFbhUU8JK8mPhwYqMwy1DRrKP8fwUwnQMY',
      amount: 10,
      unit: 'boson'
    }],
    to: [{
      address: 'acWmVcNrHzxBF8L25vdiKLsz664ZGkYmPRj',
      amount: 10,
      unit: 'boson'
    }]
  };
  const opt = {
    type: Transaction.SEND_TYPE
  };

  myTx = new Transaction(myTx, opt);
  myTx.sign()
    .then(signature => {
      // will return a string 'EB31F32425FA5FCB030B6FDF40B5A2F7598652AF897D64CA3A09121DBF0F59713FBEA213B0C9D5DCDB56746F2DF22EA4170451714CA3949F22BEBA7DB4C4F00C'
      const signatories = [{
        signature, publicKey: '<enter_public_key>'
      }]
      return newTxn.broadcast(signatories);
    })
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: { TxHash: 'C1SpcgCUdV21MHjs6ShtfYJpAiI=' },
      //     id: '81f28344-2243-384a-e014-221d11d4b4a8',
      //     jsonrpc: '2.0'
      //   }
      // }
    });


signNBroadcast
==============

**Returns:**

a

**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})


send
====

**Returns:**

.. code-block:: javascript

  const Transaction = intergallactic.Txn;
  const myTx = {
    from: [{
      address: 'acFbhUU8JK8mPhwYqMwy1DRrKP8fwUwnQMY',
      amount: 10,
      unit: 'boson'
    }],
    to: [{
      address: 'acQUFGxsXVPSd6vbAceSkURnWhYhApE9VRe',
      amount: 10
    }]
  };
  const opt = {
    type: Transaction.SEND_TYPE
  };

  myTx = new Transaction(myTx, opt);
  myTx.sign()
    .then(signature => {
      // will return a string 'EB31F32425FA5FCB030B6FDF40B5A2F7598652AF897D64CA3A09121DBF0F59713FBEA213B0C9D5DCDB56746F2DF22EA4170451714CA3949F22BEBA7DB4C4F00C'
      const signatories = [{
        signature, publicKey: '<enter_public_key>'
      }]
      return newTxn.send(signatories);
    })
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: { TxHash: 'C1SpcgCUdV21MHjs6ShtfYJpAiI=' },
      //     id: '81f28344-2243-384a-e014-221d11d4b4a8',
      //     jsonrpc: '2.0'
      //   }
      // }
    });


**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})


call
====

**Returns:**

a

**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})


bond
====

**Returns:**

a

**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})


unbond
======

**Returns:**

a

**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})


permission
==========

**Returns:**

a

**Example:**

.. code-block:: javascript

const Transaction = intergallactic.Txn;
const myTx = new Transaction({})

