# Mastering Bitcoin Discussion Questions

## Chapter 1

Why doesn't bitcoin have a hierarchical network?

What is the difference between the bitcoin network and bitcoin as a currency?

What is the double-spend problem and how did bitcoin solve it?

What determines the rate of inflation in bitcoin?

Do you think it would be better if bitcoin transactions were reversible?

Do you believe that bitcoin needs to be competitive with visa/mastercard to succeed?


## Chapter 2

What are transaction inputs and outputs and what do they have to do with the transfer of value?

Why is a transaction fee needed and how is it calculated?

Why will many bitcoin transactions include an output controlled by the sender, in addition to the output paying the receiver?  When would this not occur?

What is a mining pool and why would someone belong to one?

What is the status of a transaction that has not yet been included in a block, but has been propagated around the network? Why do some services require 6 confirmations to clear funds?"

What kind of privacy is there for transactions on a public ledger?


## Chapter 3

What are Bitcoin Improvement Proposals (BIPs) and what role do they play in determining the Bitcoin protocol?

Why is Bitcoin Core referred to as the reference implementation? Are there other widely used implementations?

What are some common reasons you would run your own full node?

What is the difference between a pruned node and a full (AKA archival) node?

## Chapter 4

What is the relationship between private keys, signatures, and witnesses?

The public key is represented by an address. Why do we need addresses and just not send bitcoin to public keys?

What is a one-way cryptographic function and how do we use it to derive public keys?

Bonus: What are some ways that private keys have been broken because of lack of entropy?

How do we know that the discrete log problem is hard to break?

Bitcoin uses the elliptic curve over a finite field of primer order. What does that mean using common English terms? Why is the order prime?

Why would we use Base58 for addresses rather than Base64? Would you make any modifications beyond Base58?

What is a checksum and how are they used in Bitcoin addresses?

Why is a compressed private key a misnomer?

What is the difference between P2PKH and P2SH?

What is the difference between a hot wallet and cold storage?


## Chapter 5

Why does address re-use reduce privacy? Can you think of other de-anonymizing missteps that might happen due to bad user-experience design or lack of privacy education?

Why does the author argue that BIP32 wallets are a superior wallet?

Bonus: Are there wallets with mnemonic seeds in languages other than English? Why is this a good or not a good idea?

Why is a brainwallet not secure, but mnemonic code words are?

What are the 3 items needed to generate children keys from a parent key? Is there a limit as to how many times this can be done? What combination of the 3 items makes up an extended key?

What are the differences between a hardened parent key and a normal parent key?

## Chapter 6

When people refer to the bitcoin ledger or a wallet that displays a received bitcoin balance, what is actually being monitored to come up with those numbers?

What are some instances when you'd need to use serialization to transmit information over the network or between applications?

Because the value of the input is not explicitly in the transaction, we must reference the UTXO set in order to calculate the fees. Why isn't this information just included in the transaction? Is there a better way to do this?

What are the two purposes of transaction fees?

Bonus: Find an instance where someone mistakenly left a very big fee for a miner. What happened and what was the outcome?

Is SCRIPT's Turing incompleteness a feature or a deficiency?

Why are the locking and unlocking scripts executed separately?

Bonus: Besides signing transactions, what are some other uses of digital signatures?

What are SIGHASH flags and how can they be used?

What would be a way to trick someone into revealing their private key by signing two things?


## Chapter 7

There is a bug in the CHECKMUTLISIG opcode. Why don't we just fix it?

P2SH shifts the burden of fees and complexity from the sender to the spender? Why would you want to do this?

Timelocks (nlocktime) are used to lock funds until a certain time or blockheight after which they are valid. Is it possible to invalidate transactions after a certain time or blockheight?

Provide a scenario that you'd personally use a multisig transaction for.

## Chapter 8

Do SPV nodes help or hurt the network?

Bonus: How many nodes are on the Bitcoin network today.

The Bitcoin Relay Network section describes multiple projects intended to reduce block propagation latency. Why is so much effort being put into this?

How do new nodes discover peers on the network?

What are the privacy concerns of using an SPV node?

Bonus: What is TOR and how does it provide privacy?

What happened to the original proposal to add p2p encryption (BIP150/151)?


## Chapter 9

The genesis block contains a hidden message within it. What OP_CODE is used to this and what are some other examples of this OP_CODE being used? Do you think superfluous data should be allowed in the blockchain?

How much data would be required to calculate a Merkle path for a tree with 4 transactions?

What is signet and how is it different than testnet and regtest?

Bonus: Bloom filters have some problems, how are block filters better?


## Chapter 10

How does mining solve the Byzantine Generals Problem?

What happens to a transaction that isn't validated by your node?

What happens if a miner tries to pay itself a higher subsidy than allowed?

In 2016, there was ~3 EH/sec of processing power. Today there are 150 EH/sec. What is the right threshold for securing the network? Can you have too much security?

Under what circumstances would a node receive an orphan block? Why would it not be discarded if its parent hasn't been received? How long should a node wait? Do you see any problems with keeping it for a long time?

A 10-minute block interval was set by Satoshi. Is that too slow? How might we speed it up? What problems might be caused by a shorter interval?

How is work by a miner monitored by pools? Could this be gamed?

Bonus: How do p2pools work? Why is this not the main method used?

Bonus: What are the largest pools today and what risk do they pose?

What prevents miners from signaling that they will support an upgrade but later not enforce it?

Upgrades have become increasingly more difficult to get merged and accepted by the community. Should we make it easier? If so, how?

## Chapter 11

Bitcoin's security relies on decentralized control over keys and on independent transaction validation by miners. Are there instances when centralization might be appropriate or even encouraged?

How do developers of the protocol fit into the trust model? What safeguards are in place to ensure there are not any single points of failure?

How can we protect ourselves from the thousands of software components that run on our personal computers?

## Chapter 12

What do you see as the biggest weakness of the Lightning Network?

Do you think the punishment mechanism in the Lightning Network incentivized the right kind of behavior?

People say that the Lightning Network is better for privacy, but each node has a persistent identity, so how is that possible?

Lightning sounds complicated. Couldn't we just use unidirectional payment channels? It's not like my coffee shop will ever be paying me, right?