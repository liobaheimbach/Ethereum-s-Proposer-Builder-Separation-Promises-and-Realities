# Ethereum's Proposer-Builder Separation: Promises and Realities 

This repository provides the aggregate data set created for the paper [Ethereum's Proposer-Builder Separation: Promises and Realities](https://arxiv.org/abs/2305.19037).

The aggregate data set is provided in four files: 
- data.pkl is a pandas dataframe with block level PBS data
- relaysBlockDict.pickle is a dictionary that indicates for each block which relay(s) claim it
- relaysDict.pickle is a dictionary that indicates for each relay which blocks it claims
- privateNonPBS.pkl is a pandas dataframe with all private transactions in non-PBS blocks

We further provide the scripts used for the data analysis in the following notebook: PBSAnalysis.ipynb.

## Builder and Seacher Addresses

We provide a map from the builder name to their Ethereum fee recipient address and public key for the biggest 17 builders in terms of the number of blocks built. Notably, we do not have a fee recipient address for Builder 3 and Builder 6 as these builders always note down the proposer address as the fee recipient. Thus, we find no trace of these builders on the Ethereum blockchain. 

| Name                | Address                                      | Public Key |
|---------------------|----------------------------------------------|------------|
| beaverbuild        | 0x95222290dd7278aa3ddd389cc1e1d165cc4bafe5  | 0x96a59d355b1f65e270b29981dd113625732539e955a1beeecbc471dd0196c4804574ff871d47ed34ff6d921061e9fc27 <br> 0xb5d883565500910f3f10f0a2e3a031139d972117a3b67da191ff93ba00ba26502d9b65385b5bca5e7c587273e40f2319 <br> 0x8dde59a0d40b9a77b901fc40bee1116acf643b2b60656ace951a5073fe317f57a086acf1eac7502ea32edcca1a900521 <br> 0xaec4ec48c2ec03c418c599622980184e926f0de3c9ceab15fc059d617fa0eafe7a0c62126a4657faf596a1b211eec347 |
| bloXroute (M)      | 0xf2f5c73fa04406b1995e397b55c24ab1f3ea726c  | 0x94aa4ee318f39b56547a253700917982f4b737a49fc3f99ce08fa715e488e673d88a60f7d2cf9145a05127f17dcb7c67 <br> 0x976e63c505050e25b70b39238990c78ddf0948685eb8c5687d17ba5089541f37dd3c45999f2db449eac298b1d4856013 <br> 0x8b8edce58fafe098763e4fabdeb318d347f9238845f22c507e813186ea7d44adecd3028f9288048f9ad3bc7c7c735fba <br> 0xaa1488eae4b06a1fff840a2b6db167afc520758dc2c8af0dfb57037954df3431b747e2f900fe8805f05d635e9a29717b |
| bloXroute (R)      | 0x199d5ed7f45f4ee35960cf22eade2076e95b253f  | 0x80c7311597316f871363f8395b6a8d056071d90d8eb27defd14759e8522786061b13728623452740ba05055f5ba9d3d5 <br> 0xb9b50821ec5f01bb19ec75e0f22264fa9369436544b65c7cf653109dd26ef1f65c4fcaf1b1bcd2a7278afc34455d3da6 <br> 0x965a05a1ba338f4bbbb97407d70659f4cea2146d83ac5da6c2f3de824713c927dcba706f35322d65764912e7756103e2 |
| bloXroute (E)      | 0xf573d99385c05c23b24ed33de616ad16a43a0919  | 0xb086acdd8da6a11c973b4b26d8c955addbae4506c78defbeb5d4e00c1266b802ff86ec7457c4c3c7c573fa1e64f7e9e0 <br> 0x95701d3f0c49d7501b7494a7a4a08ce66aa9cc1f139dbd3eec409b9893ea213e01681e6b76f031122c6663b7d72a331b <br> 0x82801ab0556f7df1fb9bb3a61ca84beea8285a8dc3c455a7ea16a8b2993fe06058e0e7d275b28ea5d9f2ae995aa72605 |
| blocknative       | 0xbaf6dc2e647aeb6f510f9e318856a1bcd66c5e19  | 0x8000008a03ebae7d8ab2f66659bd719a698b2e74097d1e423df85e0d58571140527c15052a36c19878018aaebe8a6fea <br> 0x9000009807ed12c1f08bf4e81c6da3ba8e3fc3d953898ce0102433094e5f22f21102ec057841fcb81978ed1ea0fa8246 <br> 0xa66f3abc04df65c16eb32151f2a92cb7921efdba4c25ab61b969a2af24b61508783ceb48175ef252ec9f82c6cdf8d8fd <br> 0xa00000a975dffbd1ef61953ac6c90b52b70eb0188eb9d030774346c9248f81e875f7e8bc56c4bbbda297a9543cfa051d |
| builder0x69       | 0x690b9a9e9aa1c9db991c7721a92d351db4fac990  | 0x8bc8d110f8b5207e7edc407e8fa033937ddfe8d2c6f18c12a6171400eb6e04d49238ba2b0a95e633d15558e6a706fbe4 <br> 0xb194b2b8ec91a71c18f8483825234679299d146495a08db3bf3fb955e1d85a5fca77e88de93a74f4e32320fc922d3027 <br> 0xa971c4ee4ac5d47e0fb9e16be05981bfe51458f14c06b7a020304099c23d2d9952d4254cc50f291c385d15e7cae0cf9d <br> 0xa4fb63c2ceeee73d1f1711fadf1c5357ac98cecb999d053be613f469a48f7416999a4da35dd60a7824478661399e6772 |
| Builder 1         | 0x473780deaf4a2ac070bbba936b0cdefe7f267dfc  | 0xa1daf0ab37a9a204bc5925717f78a795fa2812f8fba8bda10b1b27c554bd7dedd46775106facd72be748eea336f514e9 <br> 0x89783236c449f037b4ad7bae18cea35014187ec06e2daa016128e736739debeafc5fe8662a0613bc4ca528af5be83b3c |
| Builder 2         | 0xbd3afb0bb76683ecb4225f9dbc91f998713c3b01  | 0x82ba7cadcdfc1b156ba2c48c1c627428ba917858e62c3a97d8f919510da23d0f11cf5db53cb92a5faf5de7d31bf38632 |
| Builder 2     | 0xbd3afb0bb76683ecb4225f9dbc91f998713c3b01  | 0x82ba7cadcdfc1b156ba2c48c1c627428ba917858e62c3a97d8f919510da23d0f11cf5db53cb92a5faf5de7d31bf38632  |
| Builder 3     |                                               | 0xafc9274fe595e8cff421ab9e73b031f0dff707ea1852e2233ff070ef18e3876e25c44a9831c4b5f802653d4678ccc31f  |
| Builder 4     | 0x3b7faec3181114a99c243608bc822c5436441fff  | 0xa1f10d66aa4b73c5d9a6cc38a098b2c6ce031a6750ea2da01918ba3ac57c2ce1e39a0da622bd8ccd7c9930861f949fa2  |
| Builder 5     | 0xb646d87963da1fb9d192ddba775f24f33e857128  | 0x8bcd1148e83d0a844d2d42f90df0837dbe407055367b3bfcf04227e47ea65a0164fc13a66584aae286f8f7322dc69501  |
| Builder 6     |                                               | 0xa25f5d5bd4f1956971bbd6e5a19e59c9b1422ca253587bbbb644645bd2067cc08fb854a231061f8c91f110254664e943  |
| Eden          | 0xaab27b150451726ec7738aa1d0a94505c8729bd1  | 0x8e39849ceabc8710de49b2ca7053813de18b1c12d9ee22149dac4b90b634dd7e6d1e7d3c2b4df806ce32c6228eb70a8b <br> 0xa5eec32c40cc3737d643c24982c7f097354150aac1612d4089e2e8af44dbeefaec08a11c76bd57e7d58697ad8b2bbef5 <br> 0x91970c2db7c12510acb2e9c45844f7de602f83a7f31064f7ca04a807b607d7aebfc0abda73c036a92e5c3e56ebca04b7 <br> 0xa412007971217a42ca2ced9a90e7ca0ddfc922a1482ee6adf812c4a307e5fb7d6e668a7c86e53663ddd53c689aa3d350  |
| eth-builder   | 0xfeebabe6b0418ec13b30aadf129f5dcdd4f70cea  | 0x8eb772d96a747ba63af7acdf92dc775a859f76a77e4c6ed124dca6360e74e4e798a75a925eb8fd0dde866317fff18ad0 <br> 0x8ea1393f49d894ae22ec86e38d9aeb64b8336dac947e69cb8468acf510d010ce0b51b21ac3e1244bdb91c52e020ea525  |
| Flashbots     | 0xb64a30399f7F6b0C154c2E7Af0a3ec7B0A5b131a <br> 0xdafea492d9c6733ae3d56b7ed1adb60692c98bc5  | 0x81babeec8c9f2bb9c329fd8a3b176032fe0ab5f3b92a3f44d4575a231c7bd9c31d10b6328ef68ed1e8c02a3dbc8e80f9 <br> 0x81beef03aafd3dd33ffd7deb337407142c80fea2690e5b3190cfc01bde5753f28982a7857c96172a75a234cb7bcb994f <br> 0xa1dead01e65f0a0eee7b5170223f20c8f0cbf122eac3324d61afbdb33a8885ff8cab2ef514ac2c7698ae0d6289ef27fc  |
| Manta-builder | 0x5f927395213ee6b95de97bddcb1b2b1c0f16844f  | 0xa0d0dbdf7b5eda08c921dee5da7c78c34c9685db3e39e81eb91da94af29eaa50f1468813c86503bf41b4b51bf772800e <br> 0xb1b734b8dd42b4744dc98ea330c3d9da64b7afc050afed96875593c73937d530a773e35ddc4b480f9d2e1d5ba452a469 <br> 0xb5a688d26d7858b38c44f44568d68fb94f112fc834cd225d32dc52f0277c2007babc861f6f157a6fc6c1dc25bf409046  |
| rsync-builder | 0x1f9090aae28b8a3dceadf281b0f12828e676c326  | 0x978a35c39c41aadbe35ea29712bccffb117cc6ebcad4d86ea463d712af1dc80131d0c650dc29ba29ef27c881f43bd587 <br> 0x83d3495a2951065cf19c4d282afca0a635a39f6504bd76282ed0138fe28680ec60fa3fd149e6d27a94a7d90e7b1fb640 <br> 0x945fc51bf63613257792926c9155d7ae32db73155dc13bdfe61cd476f1fd2297b66601e8721b723cef11e4e6682e9d87  |


## Attribution
If using this repository for research, please cite as: 
``` bibtex
@inproceedings{heimbach2023ethereum,
  title = {Ethereum's Proposer-Builder Separation: Promises and Realities},
  author = {Heimbach, Lioba and Kiffer, Lucianna and Ferreira Torres, Christof and Wattenhofer, Roger},
  booktitle = {2023 ACM Internet Measurement Conference (IMC), Montreal, QC, Canada},
  month = oct,
  year = {2023},
}
```
