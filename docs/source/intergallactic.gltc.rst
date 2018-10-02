.. _gltc:

===================
intergallactic.gltc
===================

Gallactic node related module that helps to retrieve information of the node.

getChainId
==========
Get chainId information of the Gallactic node.

**Returns:**

``Object``: Response along with the chain details.

**Example:**

.. code-block:: javascript

  intergallactic.gltc.getChainId()
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: {
      //       ChainName: 'test-chain',
      //       ChainId: 'test-chain-8F70F3',
      //       GenesisHash: '8F70F38FB8F161A11339AAD1995C4A36A68A01375D9A1E340F884818C229BFF0'
      //     },
      //     id: '8392696f-cecf-77da-9204-02c1630fb694',
      //     jsonrpc: '2.0'
      //   }
      // }
    });


getInfo(WIP)
============
Get the node information about the Gallactic node.

**Returns:**

``Object``: Response along with the node information.

**Example:**


getLatestBlock
==============
Get the latest block information of the Gallactic node.

**Returns:**

``Object``: Response along with the latest block information.

**Example:**

.. code-block:: javascript

  intergallactic.gltc.getLatestBlock()
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: {
      //       BlockMeta: {
      //         block_id: {
      //           hash: '5D47666FA7D941532685127F85110534FA76936C',
      //           parts: {
      //             total: '1',
      //             hash: 'C9D48BF0910418044EB2982D371BADF4A01F081C'
      //           }
      //         },
      //         header: {
      //           chain_id: 'test-chain-8F70F3',
      //           height: '63004',
      //           time: '2018-09-13T03:24:02.42693163Z',
      //           num_txs: '0',
      //           last_block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           total_txs: '0',
      //           last_commit_hash: '8779B52550A109AFA3CB975CB49EEBC6ECBB0215',
      //           data_hash: '',
      //           validators_hash: '28C203B50AFBA0BB3F97FCB74DCF9856E4F8C701',
      //           consensus_hash: 'D6B74BB35BDFFD8392340F2A379173548AE188FE',
      //           app_hash: '9234B012E8A146F5C3C723367EA3292006BE1250',
      //           last_results_hash: '',
      //           evidence_hash: ''
      //         }
      //       },
      //       Block: {
      //         header: {
      //           chain_id: 'test-chain-8F70F3',
      //           height: '63004',
      //           time: '2018-09-13T03:24:02.42693163Z',
      //           num_txs: '0',
      //           last_block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           total_txs: '0',
      //           last_commit_hash: '8779B52550A109AFA3CB975CB49EEBC6ECBB0215',
      //           data_hash: '',
      //           validators_hash: '28C203B50AFBA0BB3F97FCB74DCF9856E4F8C701',
      //           consensus_hash: 'D6B74BB35BDFFD8392340F2A379173548AE188FE',
      //           app_hash: '9234B012E8A146F5C3C723367EA3292006BE1250',
      //           last_results_hash: '',
      //           evidence_hash: ''
      //         },
      //         data: { txs: null },
      //         evidence: { evidence: null },
      //         last_commit: {
      //           block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           precomits: [{
      //             validator_address: '12FFF6E1E2071423B1ED41BC9D4761DD1804C9B3',
      //             validator_index: '0',
      //             height: '64314',
      //             round: '0',
      //             timestamp: '2018-09-13T03:47:33.455045753Z',
      //             type: 2,
      //             block_id:
      //             {
      //               hash: '426D35D41C0533F0DD1877F0CAF9458716C4124A',
      //               parts: {
      //                 total: '1',
      //                 hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //               }
      //             },
      //             signature:
      //             {
      //               type: 'tendermint/SignatureEd25519',
      //               value: 'P90Pf9gNQ0MX6UsFu6UVT/6vj1wFznfJJIyphn6ZHzbTerltpttSWvpZQ8dK6l91D0eZw91tk9RcKhOautSYCw=='
      //             }
      //           }]
      //         }
      //       }
      //     },
      //     id: 'd698a8b8-11cb-96e9-282d-595fa328ce75',
      //     jsonrpc: '2.0'
      //   }
      // }
    });


getBlock
========
Get a block information of the Gallactic node given height of the block.

**Parameters:**

``number`` (required) : a number that represents the block height in the node.

**Returns:**

``Object``: Response along with the latest block information.

**Example:**

.. code-block:: javascript

  intergallactic.gltc.getBlock(63004) // 63004 as in the block height
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: {
      //       BlockMeta: {
      //         block_id: {
      //           hash: '5D47666FA7D941532685127F85110534FA76936C',
      //           parts: {
      //             total: '1',
      //             hash: 'C9D48BF0910418044EB2982D371BADF4A01F081C'
      //           }
      //         },
      //         header: {
      //           chain_id: 'test-chain-8F70F3',
      //           height: '63004',
      //           time: '2018-09-13T03:24:02.42693163Z',
      //           num_txs: '0',
      //           last_block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           total_txs: '0',
      //           last_commit_hash: '8779B52550A109AFA3CB975CB49EEBC6ECBB0215',
      //           data_hash: '',
      //           validators_hash: '28C203B50AFBA0BB3F97FCB74DCF9856E4F8C701',
      //           consensus_hash: 'D6B74BB35BDFFD8392340F2A379173548AE188FE',
      //           app_hash: '9234B012E8A146F5C3C723367EA3292006BE1250',
      //           last_results_hash: '',
      //           evidence_hash: ''
      //         }
      //       },
      //       Block: {
      //         header: {
      //           chain_id: 'test-chain-8F70F3',
      //           height: '63004',
      //           time: '2018-09-13T03:24:02.42693163Z',
      //           num_txs: '0',
      //           last_block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           total_txs: '0',
      //           last_commit_hash: '8779B52550A109AFA3CB975CB49EEBC6ECBB0215',
      //           data_hash: '',
      //           validators_hash: '28C203B50AFBA0BB3F97FCB74DCF9856E4F8C701',
      //           consensus_hash: 'D6B74BB35BDFFD8392340F2A379173548AE188FE',
      //           app_hash: '9234B012E8A146F5C3C723367EA3292006BE1250',
      //           last_results_hash: '',
      //           evidence_hash: ''
      //         },
      //         data: { txs: null },
      //         evidence: { evidence: null },
      //         last_commit: {
      //           block_id: {
      //             hash: 'FE70989F920DFDB6254C74B7B9BE38DDC36616BA',
      //             parts: {
      //               total: '1',
      //               hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //             }
      //           },
      //           precomits: [{
      //             validator_address: '12FFF6E1E2071423B1ED41BC9D4761DD1804C9B3',
      //             validator_index: '0',
      //             height: '64314',
      //             round: '0',
      //             timestamp: '2018-09-13T03:47:33.455045753Z',
      //             type: 2,
      //             block_id:
      //             {
      //               hash: '426D35D41C0533F0DD1877F0CAF9458716C4124A',
      //               parts: {
      //                 total: '1',
      //                 hash: 'BA09FC4D0C9CBEEAC3C4E671A5152D79656B2FAC'
      //               }
      //             },
      //             signature:
      //             {
      //               type: 'tendermint/SignatureEd25519',
      //               value: 'P90Pf9gNQ0MX6UsFu6UVT/6vj1wFznfJJIyphn6ZHzbTerltpttSWvpZQ8dK6l91D0eZw91tk9RcKhOautSYCw=='
      //             }
      //           }]
      //         }
      //       }
      //     },
      //     id: 'd698a8b8-11cb-96e9-282d-595fa328ce75',
      //     jsonrpc: '2.0'
      //   }
      // }
    });

getBlockTxns
============
Get the transaction information of a block given block height.

**Returns:**

``Object``: Response along with the latest block information.

**Example:**

.. code-block:: javascript

  intergallactic.gltc.getBlockTxns()
    .then(res => {
      // res = {
      //   statusCode: 200,
      //   body: {
      //     result: { Count: 0, Txs: [] },
      //     id: '81f28344-2243-384a-e014-221d11d4b4a8',
      //     jsonrpc: '2.0'
      //   }
      // }
    });
