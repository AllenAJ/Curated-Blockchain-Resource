---
description: Frequently Asked Questions (F.A.Q.s) & Answers
---

# FAQ

**Q: What's a Blockchain?**

A: A blockchain is a distributed database with a list \(that is, chain\) of records \(that is, blocks\) linked and secured by digital fingerprints \(that is, crypto hashes\). Example from [`genesis_block.json`](https://github.com/yjjnls/awesome-blockchain/tree/master/src/js/genesis_block.json):

```text
{
    "version": 0,
    "height": 1,
    "previous_hash": null,
    "timestamp": 1550049140488,
    "merkle_hash": null,
    "generator_publickey": "18941c80a77f2150107cdde99486ba672b5279ddd469eeefed308540fbd46983",
    "hash": "d611edb9fd86ee234cdc08d9bf382330d6ccc721cd5e59cf2a01b0a2a8decfff",
    "block_signature": "603b61b14348fb7eb087fe3267e28abacadf3932f0e33958fb016ab60f825e3124bfe6c7198d38f8c91b0a3b1f928919190680e44fbe7289a4202039ffbb2109",
    "consensus_data": {},
    "transactions": []
}
```

[![](https://github.com/yjjnls/awesome-blockchain/raw/master/Basic/img/blockchain-jesus.png)](https://github.com/yjjnls/awesome-blockchain/blob/master/Basic/img/blockchain-jesus.png)

**Q: What's a Hash? What's a \(One-Way\) Crypto\(graphic\) Hash Digest Checksum**?

A: A hash e.g. `d611edb9fd86ee234cdc08d9bf382330d6ccc721cd5e59cf2a01b0a2a8decfff` is a small digest checksum calculated with a one-way crypto\(graphic\) hash digest checksum function e.g. SHA256 \(Secure Hash Algorithm 256 Bits\) from the data. Example from [`crypto.js`](https://github.com/yjjnls/awesome-blockchain/blob/master/src/js/crypto.js):

```text
function calc_hash(data) {
    return crypto.createHash('sha256').update(data).digest('hex');
}
```

A blockchain uses

* the block header \(e.g. `Version`, `TimeStamp`, `Previous Hash...` \)and
* the block data \(e.g. `Transaction Data...`\)

to calculate the new hash digest checksum.

**Q: What's a Merkle Tree?**

A: A Merkle tree is a hash tree named after Ralph Merkle who patented the concept in 1979 \(the patent expired in 2002\). A hash tree is a generalization of hash lists or hash chains where every leaf node \(in the tree\) is labelled with a data block and every non-leaf node \(in the tree\) is labelled with the crypto\(graphic\) hash of the labels of its child nodes. For more see the [Merkle tree](https://en.wikipedia.org/wiki/Merkle_tree) Wikipedia Article.

Note: By adding crypto\(graphic\) hash functions you can "merkelize" any data structure.

**Q: What's a Merkelized DAG \(Directed Acyclic Graph\)?**

A: It's a blockchain secured by crypto\(graphic\) hashes that uses a directed acyclic graph data structure \(instead of linear "classic" linked list\).

Note: Git uses merkelized dag \(directed acyclic graph\)s for its blockchains.

**Q: Is the Git Repo a Blockchain?**

A: Yes, every branch in the git repo is a blockchain. The "classic" Satoshi-blockchain is like a git repo with a single master branch \(only\).  


**More Q&A**

* [Blockchain Interview Questions](https://mindmajix.com/blockchain-interview-questions)
* [10 Essential Blockchain Interview Questions](https://www.toptal.com/blockchain/interview-questions)
* [Top 36 Blockchain Job Interview Questions & Answers](https://blockchainsfactory.com/blockchain-interview-questions/)

