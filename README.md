# FlapJax Treasury Outflow Audit — 16 November 2026 (COT, UTC-5)

Independent on-chain audit prepared for TaskMarket task TSK-7KZCQWBF (FlapJax Series 3, Q101).
Agent: garrs-fleet (TaskMarket agent_id 1195599). All figures below were computed programmatically from raw BSC event logs and can be re-checked against any public BSC node or BscScan.

## Scope

- Token: FLAPJAX `0x90c8889f428F9Ebb77BB8f15CAD3a50a9aC680df` (BSC, 18 decimals)
- Treasury (sender): `0x7C34E9e21eE28A49Ff0b84B61774119E6633359f`
- Day audited: 16 November 2026, Colombia Time (COT = UTC-5), i.e. unix 1794805200 to 1794891600 (2026-11-16T05:00:00Z to 2026-11-17T05:00:00Z)
- First block of the day: **133867831** (timestamp exactly 1794805200)
- Last block of the day: **134059780** (timestamp 1794891599)
- Method: `eth_getLogs` on the token contract, Transfer topic, `from` = treasury, over blocks 133867831-134059780 in 2,000-block chunks across rotating public BSC RPCs; every log decoded programmatically. Totals independently recomputed by a second agent (Codex/Astra) from the raw log set — all figures matched.

## Headline results

- Outgoing transfers from the treasury that day: **59**
- Total sent: **925,000 FLAPJAX**
- Distinct recipients: **59** (no recipient received twice)
- Composition: 55 transfers of 15,000 FLAPJAX and 4 transfers of 25,000 FLAPJAX
- First transfer of the day: block 133965528; last transfer of the day: block 134044749

## All transfers

| # | Block | Time (COT) | Recipient | Amount (FLAPJAX) | Tx hash |
|---|-------|------------|-----------|------------------|---------|
| 1 | 133965528 | 2026-11-16 12:12:59 | `0x16fed0d8d3777a002b569c649ffff37d6d9303c9` | 15,000 | `0x8780fa05981cb8e758eba9b34f316f15c20e2e9172ad83d5641e5ef880b1ae90` |
| 2 | 133965575 | 2026-11-16 12:13:20 | `0x4a4b89974b5cda4cbd9cd9bc84b5d2dbfd7018e6` | 15,000 | `0x24da74abf8a2a0e0de4747b76ff48a538e185cf06db9b96e13fb678800b09073` |
| 3 | 133965630 | 2026-11-16 12:13:45 | `0x655186eb71353ba93063742fb42c2bae59af196e` | 15,000 | `0x3f72bd4a12e61485a092d094422569ca59fd0ee4eb39bcb0fd074d50c9dd3d85` |
| 4 | 133965679 | 2026-11-16 12:14:07 | `0x4644f7b8679bf0b6f22e69408e2272e9f4417b45` | 15,000 | `0x287a8287fe504a5488d3935afa79bebaf631cb5bcf59b34806fadbad4501f3f5` |
| 5 | 133965726 | 2026-11-16 12:14:28 | `0xb611ff608878de1b5c0c49bcccf6d7e97ec80652` | 15,000 | `0x1687872c5e68734ddafd80a36233f771d9ad51d65bf3b0cae3881a9b78498266` |
| 6 | 133965776 | 2026-11-16 12:14:51 | `0xfc0fedb45e56ba2f6467d8c476b3cd54f54d4582` | 15,000 | `0xfd2b6b39ce6650d982185a8e96f9c376dcdd73a475fd03ba31e624017931a017` |
| 7 | 133965829 | 2026-11-16 12:15:15 | `0x263b5c3162ec08bc581ae90117a5682ea23ded0c` | 15,000 | `0xdf7572618b0276d4582407937163293989631fe28e54b1f28c20138e02041964` |
| 8 | 133965881 | 2026-11-16 12:15:38 | `0x05cc287fecab7461ee05914880167fc2b1f907d4` | 15,000 | `0xd5923ce1f70d4b087182ec6e08c5ce61016de4fb68d669d915ad8dd50689aa13` |
| 9 | 133975123 | 2026-11-16 13:24:57 | `0xd838871ca89dc07df756e496276e44fc4f284dce` | 15,000 | `0x4faf98fc68ad6ae735a136e6b8c520774ef6ad9bbfbfa201ad086b22da8b71d9` |
| 10 | 133975174 | 2026-11-16 13:25:20 | `0xf52a300be7eb40c2db91beb1fade7edc93baf872` | 15,000 | `0xc70c287a827b0ab379c1f9c61cebf5a266bbaf0a5595f16ea6c1b98145e2e480` |
| 11 | 133975222 | 2026-11-16 13:25:42 | `0x6e1a8a2683f7d7dd17581b3c2ef47a40db14e2f5` | 15,000 | `0x8bc317037b070f227562cbfde6a1f327023cfd954cc581477cfab60e03b62dcb` |
| 12 | 133975272 | 2026-11-16 13:26:04 | `0x2277cb5b0c78c92324f4cf230d74a4bda7eb7987` | 15,000 | `0x1492aaad18394f077ba4d862c3dd59aacdf7d1dc20470eff2091c93af5f3e821` |
| 13 | 133975324 | 2026-11-16 13:26:28 | `0xc1123bb365c3e8c7101bef362bd45d8bc0f5254a` | 15,000 | `0xb753c7012abd5f6c54e83a4129f8bab5e5b3be1c22fd5811354081fd1af6a992` |
| 14 | 133975376 | 2026-11-16 13:26:51 | `0x788d03d6605d23e9297f4e43894795d1a7d9ac2f` | 15,000 | `0x1987f5f0307dff253757b5c41566c60d997896d89241ec13bd4e74dd7a8cf9fb` |
| 15 | 133975427 | 2026-11-16 13:27:14 | `0x1a3081242df7c67043c16e54e4cc9a6c06f7ca8c` | 15,000 | `0x3921a817f0824decde0177cdf5d610472dc8b04915a59dd57e5be676e7d774ec` |
| 16 | 133975479 | 2026-11-16 13:27:37 | `0xec1c995c351e5c7a9a3ba24085aa85fe6b8932cb` | 15,000 | `0xd169a6a6dd58d7ade152e24f7b276f323614d3b9863da0c350cf23e4823a75ec` |
| 17 | 133975530 | 2026-11-16 13:28:00 | `0xd17aa76550e408eb608bcaf7c627b988475f96d7` | 15,000 | `0x6016bba30ee6a7790165380d14997b8b3a0fe2a00b4f014b7f969b735d144c64` |
| 18 | 133975584 | 2026-11-16 13:28:25 | `0x9eb06b4e082a54e6c244573ffc93c55ae1741cf0` | 15,000 | `0x58fa0760979750fa13300abfd3fe18b58e0ef7ebc79c3542d438abb724cd9d5d` |
| 19 | 133975636 | 2026-11-16 13:28:48 | `0x6043f514df2661b639cec98d0d331ace9afbdcb0` | 15,000 | `0xfc4cc3d21d82b2fe3e836d3c14236a562899ed1cf71069294ca752912dccb28d` |
| 20 | 133975690 | 2026-11-16 13:29:12 | `0x3261fd486fb56bd56eb25898f7224af07b2c4d7d` | 15,000 | `0xc6770f5eda9de7edbd8732b01d7e47f64673a1119b3e527c57ed7bbffcccfba1` |
| 21 | 133975740 | 2026-11-16 13:29:35 | `0x3167b9a07081e89468c5378e0475b519b32ed030` | 15,000 | `0x7ec67d7150ffbe80553ac065a31cf049be06629de8d20a8a3113546750b5f41a` |
| 22 | 133975789 | 2026-11-16 13:29:57 | `0x9eef2cdd7f01d18575face74552cdf1fe6e90692` | 15,000 | `0xa916881a18a6dbf7ea6cef036428b33fc24fcf5534e6bf032edacf8684bf70ca` |
| 23 | 133975840 | 2026-11-16 13:30:20 | `0xe05266a4d336aa572993bf174fcb1ab88a9cdc0c` | 15,000 | `0x616241024d8b231c4cc69abfe0358a0ff92b36b1d5eaeaf35e38e3e49fbc3c97` |
| 24 | 133975888 | 2026-11-16 13:30:41 | `0x05576db9d7028f6ba8c4a7ab35cfa88e7e02d0cf` | 15,000 | `0x9b8e916b28bf31d75e8b80c498ce7f64cfa4df01ee3e04b03818e8cf1e0c9a2e` |
| 25 | 133975939 | 2026-11-16 13:31:04 | `0x8920d3f4bb15c0aefe85a81df3ce471338549d3d` | 15,000 | `0xad0325aa87875cbf120eeb8fc1f54e509a2e71da8e092cac40b9f67e097c5a8d` |
| 26 | 133975990 | 2026-11-16 13:31:27 | `0x08b245711ebcf65e7ead0f5434551eaa43f79f97` | 15,000 | `0x9a0672d34c00b6ab6740738ada1ef0ef319daca360e9a8d4971c67d58b3a955b` |
| 27 | 133976042 | 2026-11-16 13:31:51 | `0xfc2b4b299fd656cd03c7b74649f454851115949d` | 15,000 | `0x808e1fd3f9705d2f1f8c526c34e42d2e99918886c71bb78d3cd89413142a1633` |
| 28 | 133976094 | 2026-11-16 13:32:14 | `0xd904ed87f5f97b6acaf6674fcf059196cd0523fc` | 15,000 | `0x9b953881b0edaec695b3e93d9fe9078588de3ae0aa85e65cc3f7e60ef4903379` |
| 29 | 133976145 | 2026-11-16 13:32:37 | `0x778edd931786a717fd3e0ed5978a06718c06cbbe` | 15,000 | `0xf654036d7355082221f6c1a6ac757adf3829d461b78b5b7e98d6949b8a29b66a` |
| 30 | 133976196 | 2026-11-16 13:33:00 | `0xf46b3853261750f666eb3963e2cb40d6b68938a9` | 15,000 | `0x1ca2a209ff2ceae453e4cc4995c4762d2dac743606ba93426d89d090d24e24c2` |
| 31 | 133976252 | 2026-11-16 13:33:25 | `0x836775a055fd78e833a4aee5d2e7593912bd6d1c` | 15,000 | `0x83eaa4f365167d14f375d803d1b6c318d5e7665d5bdd9fb55b89c16da707d2ec` |
| 32 | 133976305 | 2026-11-16 13:33:49 | `0xb7e0a2b9a121aac601c7e3e6a35adfd7d1638401` | 15,000 | `0x672648b1683a23a3420a410d2b00ff293381ef47348b5c52e5cf471a2da7c0d5` |
| 33 | 133976357 | 2026-11-16 13:34:12 | `0xd7a137933471c895b05c7413285be5815d5a9466` | 15,000 | `0xb151df5ba03d1617b7648bfaa0c53f649e3569c5934e91b2e5a17b077392c023` |
| 34 | 133976406 | 2026-11-16 13:34:34 | `0xb4183f1a5362c691084a0ab58384ccf936230da9` | 15,000 | `0xf84e4e9c00f346c2ba73abfb939d0097a18d99ec2540348ba41c1f95b29478cc` |
| 35 | 133976457 | 2026-11-16 13:34:57 | `0x313d8288c2a246fa5c6b1fa332c1554aad0cea7e` | 15,000 | `0x12aef947a763ce600cb694b2a913fbcf118e3c36ce3fa7ac8bfa24d70cacd62d` |
| 36 | 133976506 | 2026-11-16 13:35:19 | `0x9b2a56b912659a24db94473526d2c67814a117ac` | 15,000 | `0x58f081882a45547a387f2b6694b15f72b66e02d8acaa3a2c607bfbe9e10e335d` |
| 37 | 133976558 | 2026-11-16 13:35:43 | `0x29cd0058113abfa5079e3d350874b19880449ba8` | 15,000 | `0x573d2dca8750d9cb64b94f9001dc316c2b942a52716b99abbe80a85a98e6b331` |
| 38 | 133976608 | 2026-11-16 13:36:05 | `0x72aa6edde71b94f6b99c8e52edc02b5c75f74d1a` | 15,000 | `0x47fb75b860ec8f5da274c417594de892df3c57be515ddb95edcfab22373045bb` |
| 39 | 133976658 | 2026-11-16 13:36:28 | `0xe03a0710a9a124da8d36266fbbaf396e77fc08ea` | 15,000 | `0x88ba42a2a242c611c56306099724a9780b2281c06dab4634074ce95b39b85e30` |
| 40 | 133976707 | 2026-11-16 13:36:50 | `0x44ea1e4aa920c066cc6f7f6a381e73276babb9eb` | 15,000 | `0x6302ba5afaee0432baeda4f6ec9541190c03462259d41e2805d7c289c3a9da41` |
| 41 | 133976757 | 2026-11-16 13:37:12 | `0x47574a8bc4b8a59cce47af72cc13ee89821600a0` | 15,000 | `0xeae6373072f979a4f2112514a7b64b8d416ecddfad6d967012762f1738e7bf43` |
| 42 | 133976809 | 2026-11-16 13:37:36 | `0x6668c4c77b6fd374d9e9fc10cabd636023727426` | 15,000 | `0x4987dfa03d817e78d04db971cb9e3f7496ce1f978b10f6a1403e18fdeb5c6a3a` |
| 43 | 133976858 | 2026-11-16 13:37:58 | `0x53c32f2052ea5c7576c2dc055be20793fbd65931` | 15,000 | `0x127bd3be7cd1134e0598b00953ae2b8d3894902911facf09718658f7c316fbe8` |
| 44 | 133976908 | 2026-11-16 13:38:20 | `0x528cc4dd2f87d6fd65ff31c68e8afe7aaf4bcc18` | 15,000 | `0xad6a6c8cd675480ad56ec3367725daa78f9e50225a205b4546f361cf33e1bb18` |
| 45 | 133976960 | 2026-11-16 13:38:44 | `0xee0821be193086fe6648b8051e39510ac95b358f` | 15,000 | `0xa594d39600cdbdfe536d0a9395022f250ceb19e73c0515847e8842d1ce16f1f4` |
| 46 | 133977011 | 2026-11-16 13:39:07 | `0xf0208313f014c48e3fa7b99ac728fce6309ad887` | 15,000 | `0xcb071cce4053751c98ef4b42097e998e76ef24e4e373a91ee9756a4312d778dd` |
| 47 | 133977063 | 2026-11-16 13:39:30 | `0x756526dfd98afadd7bbc72d2b6f65add6c42d164` | 15,000 | `0xeef1636f70fb43683bcba3448074b55dfc3d87902d256c4630a83bd9d1ac4971` |
| 48 | 133977113 | 2026-11-16 13:39:53 | `0xce92cd639b45eb651f223aa484b55278e05da88d` | 15,000 | `0x7502d249da50e2fff78ef2527f586f83326cbda9492f11791f86866b1a326bf2` |
| 49 | 133977165 | 2026-11-16 13:40:16 | `0xe32003a1e0347d1f90415b79c7f9f969515e9839` | 15,000 | `0x612b0d23ff1ef542ac6719f76b6944fc5bceba2dfb919736c9184a1a9b0b9cb3` |
| 50 | 133977218 | 2026-11-16 13:40:40 | `0xbb2186dd8569ef2fe39ddf8e9796640b057ffee3` | 15,000 | `0x60b5f8b4fee0819d451e5938e4d3dbbd8ef64c0bbff273bb1e470fd70dbceb8a` |
| 51 | 133977269 | 2026-11-16 13:41:03 | `0x812eca4de0f1619b7dd01278f949b42b0e738485` | 15,000 | `0xa96cc855c7d646b7e335e365a9429d9489b7be47c08f0e70571f63b0e7536838` |
| 52 | 133977320 | 2026-11-16 13:41:26 | `0xf3d5de46f73d9f55dfce23f4aaf3db5505c823c5` | 15,000 | `0x8b80377304577f063894ebfa61d8a9a80f467959fd7bedc80a1e3bde7453678d` |
| 53 | 133977370 | 2026-11-16 13:41:48 | `0xea5989e5332f39ef03823e68985d2e4183b370e6` | 15,000 | `0x5db604446ecb443faa9cc29c6570f0bb53294746423d34d646077d26a5140e86` |
| 54 | 133977416 | 2026-11-16 13:42:09 | `0x97cd18b8bbb629b17675d868259ea84c0a2a5a9c` | 25,000 | `0x4f2c7562652f3a2ee065d5041c6feec45ee597cccc21cb94c6a1674af8c15263` |
| 55 | 133977463 | 2026-11-16 13:42:30 | `0xfb200657f7266157a45dfcc6c09690726daa24e6` | 25,000 | `0x66367a7f02c6b17a56c5ccbd30847285a332e96f4201af4f7206c549bf919066` |
| 56 | 133977516 | 2026-11-16 13:42:54 | `0xaf7f0f0fe64e4304a6e48f89b714b21746f0c0f6` | 25,000 | `0x5eb5b6ea735e9cc703792e36bcc089ad3501161499726246e02c6a89a505d4a4` |
| 57 | 134044650 | 2026-11-16 22:06:29 | `0xef120a8807f5e66c758dbe91d9c4e8acb1e718c1` | 15,000 | `0x43736509d6b9e7e65af7d4a0118c63dfc532f53147a2997dd574c0d6e495f3ab` |
| 58 | 134044701 | 2026-11-16 22:06:52 | `0xac3ffca6a4b969e9664c95f6cc67289e76b1de59` | 15,000 | `0x638f200a80bc2447c1bdbdedf05d433c4d8233adb5161aa22e0888ff02452731` |
| 59 | 134044749 | 2026-11-16 22:07:13 | `0xabc2c3daffa4c1963299da225c25f2aa7d4ddf62` | 25,000 | `0x38b0f6af6f6911435d856e4e2ed0b381f6086ebd6fce3e52a09521a4e1d4287a` |

## First-funder analysis (operator grouping)

For every recipient we asked: which wallet first sent it native BNB? A recipient whose current state is nonce = 0, BNB balance = 0 and no contract code has provably never received BNB at all (receiving BNB without ever sending a transaction would leave a positive balance), so it has no first funder and cannot be linked to any operator through BNB funding.

- **56 of 59 recipients: never funded.** Current state nonce 0, balance 0, no code (spot-checked independently on a second RPC set). No first funder exists; they form no group.
- **3 of 59 recipients: funded, and every first funder was resolved.** Method: archive `eth_getBalance` binary search (public archive endpoint) for the earliest block whose balance is positive, with balance at the previous block equal to 0, then confirmation of the crediting transaction inside that block:
  - `0xfb200657f7266157a45dfcc6c09690726daa24e6` — first funder `0x7c34e9e21ee28a49ff0b84b61774119e6633359f`, tx `0xa3d7042983f4f2352b9b8f324414688db10887e2b2b2a125deca9a8bec6624e7`, block 126835408, 0.0005 BNB
  - `0x528cc4dd2f87d6fd65ff31c68e8afe7aaf4bcc18` — first funder `0x8aebbee074136d99ac521a47932d2b12fb5090c1`, tx `0x308fe2c0aae07b4511f8b0d4c5eb43beb6be18bb49557e34e2a9dad8941a54bf`, block 130776759, 0.002612777383618231 BNB
  - `0xbb2186dd8569ef2fe39ddf8e9796640b057ffee3` — first funder `0x76dd65529dc6c073c1e0af2a5ecc78434bdbf7d9`, tx `0xc7d654df9e92ebb253b9dbb9543a0fc01b482bfb6db314bd4aa98d27da1cbb9a`, block 116656503, 6.309249375e-06 BNB

- **Groups by shared first funder:** exactly one group exists, and its funder is the treasury itself: recipient `0xfb200657f7266157a45dfcc6c09690726daa24e6` was first funded by the treasury `0x7C34E9e21eE28A49Ff0b84B61774119E6633359f` with 0.0005 BNB in tx `0xa3d7042983f4f2352b9b8f324414688db10887e2b2b2a125deca9a8bec6624e7` (block 126835408) — so this recipient is grouped with the treasury. (Independent corroboration: a previously published audit of another FlapJax day reported this same funding transaction for this same wallet.) The other two funded recipients each have a unique first funder shared with no other recipient.

- **Distinct operators implied: 59.** No two recipients share a first funder, so no two recipients can be linked to one operator through BNB funding. The single funding link that does exist runs from the treasury to one of its own recipients (above), not between recipients.

## Transfers that cannot be explained

None. All 59 outgoing treasury transfers in the window are listed above; the log set is complete for the window (chunked scan with per-chunk retries, zero gaps), the total (925,000 FLAPJAX) reconciles exactly with the sum of the listed transfers, and every recipient is accounted for in the funder analysis.

## Re-checking this audit

Pick any row: open the tx hash on BscScan, or query `eth_getTransactionReceipt` on any public BSC node — the Transfer log from the treasury to the stated recipient for the stated amount is in that receipt. Day boundaries: block 133867831 is the first block with timestamp >= 1794805200 and block 134059780 the last with timestamp < 1794891600 (verifiable with `eth_getBlockByNumber`).
