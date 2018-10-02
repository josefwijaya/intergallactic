.. _account:

======================
intergallactic.account
======================

Interract with gallactic blockchain node related to account information.

getAccount
==========
Retrieve account details given account address.

**Returns:**

``Object``: Response along with the account details.

**Example:**

.. code-block:: javascript

  intergallactic.account.getAccount('acLmQjWRZ4XmNZ7QfydbymbKKDYRSunkTua')
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: {
      //       Account: {
      //         address: 'acLmQjWRZ4XmNZ7QfydbymbKKDYRSunkTua',
      //         sequence: 0,
      //         balance: 100,
      //         code: null,
      //         permissions: '0x0'
      //       }
      //     },
      //     id: '92b765bc-cea6-cd39-4a52-49d8ce6144be',
      //     jsonrpc: '2.0'
      //   }
      // }
    });


getStorage
==========
Retrieve storage of an account given account address.

**Returns:**

``Object``: Response along with the storage info.

**Example:**

.. code-block:: javascript

  intergallactic.account.getStorage('acLmQjWRZ4XmNZ7QfydbymbKKDYRSunkTua')
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: {
      //       StorageItems: null
      //     },
      //     id: '8392696f-cecf-77da-9204-02c1630fb694',
      //     jsonrpc: '2.0'
      //   }
      // }
    });
