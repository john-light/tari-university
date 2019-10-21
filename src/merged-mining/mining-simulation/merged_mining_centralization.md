# Merged Mining and Mining Centralization 

**Blockchain modelling: Investigate merged-mining and mining centralisation**

1. Develop models around merged-mining and mining centralization with upcoming RandomX PoW protocol for Monero, and how this may effect Tari.

## RandomX 

RandomX is a new ASIC resistant PoW algorithm. It is designred to be ASIC restistant through the use of random code execution and memory-hard techniques to prevent specialized mining hardware from dominating the network. 

## Bitcoin Mining Centralization 

While the use of proof-of-work (PoW) to solve the double spending problem was Satoshi Nakamoto's key breakthrough with Bitcoin, it is also viewed as one of the weakest points of the system in terms of its potential to be attacked. 

Someone who controls 51% of the computing power pointed at the Bitcoin network is able to choose which transactions can be processed. Someone who controls the majority of the network hashrate can also reorganise the history of network transations in a malicious attempt to spend the same money twice. 

That said, gaining such a large percentage of the network hashrate would be no easy task, seeing as current estimates put the network hashrate at around 70 million terahashes per second. 

During the future of Bitcoin minin gat the Bitcoin 2019 conference, Streng made it clear that he does not view current level of centralization in Bitcoin mining as acceptable. 

While Satoshi's orginal vision of the mining process involved the concept of one vote per computer, that optimistic vision was thrown out rahter early in Bitcoin's history. By 2012, hardware devices built for the specifdic purpose of mining Bitcpin had been developed, and Bitcoin mining was on its way towards specialization and industrialization. 

While Corallo acknowledged miners can gain an advantage by obtaining access to the cheapest electricity in the world, he also pointed out that the availability of cheap power in chunks of 10 to 100 megawatts is somewhat limited and these sorts of setups won’t necessarily account for a large chunk of the overall network hashrate.

### A New Bitcoin Mining Protocol 

Braiins announced a redesigned mining protocol as part of a new, open, and transpatent Bitcoin mining stack. 

A key aspect of this new mining protocol, known as Stratum v2, is that it allows individula miners, rather than the mining pool operators, choose which transactions go into mined blocks. 

The level of centralizatiopn found with mining pools is much worse that it is with the actual miners, so moving the process of choosing transations from the pools to the individual miners should be a boon for decentralisation. 







## Myriad Coin

- Myriad has 3 PoW and 2 merged PoW algos 
- Seems to be very 51% resistant 
- Interesting but the variance in blocktime is extreme 
- The target block rate is 1 min 
- Algos: each of the 5 Lagos has equal probability to solve the PoW, the difficulty is adjusted to 5min for each. Any algo can build on top of the longest chain, even consecutively. With the 5 algos, any 1 pool can only achieve 20% of the effience hash rate 
- Myriadcoin has 5 algorithms (SHA256d, Scrypt, Skein, Qubit, and Myriad-Groestl) that can independently solve blocks. They have independent difficulties that are adjusted using the same formula. Any algorithm can solve the next block even if it is the same algorithm. Each algorithm targets the same block time and the block r
- Having block times that are almost 50% in the low end opens you up to other attacks 

## Questions  

- Need to simulate to see if its more stable if its more active 
- parametrised sim of this approach. I suspect that it can be tuned to be far better than that data shows
- How it is affected by selfish mining- I suspect it will be fine but the sim should be able to show the effect of that
- Query: You You actually want consensus to be achieved only when every algo has a block, So perhaps 2 * num algos? Hypothesis: I think that if you get the difficulty adjustment right you don't need that. However we are speculating, a sim would answer a lot of these questions



##Notes

- Incentive to mine
- Hybrid mining, tasing power more for the merged mining 
- Two difficulties 
- It would be difficult to game? Bigger barrier to entry 
- Can’t start to mine- have to wait for the Monero chain (not ideal)
- Game theory 
- Merged miner with a lot of hash power- power is halved- need to overcome 
- Balances out- more hashing power (same on electricity used)
- Nothing stops mining pool for swapping hashing power 
- Difficulty? 
- Check myriad strategies 
- One laptop is the alternate miner- difficulty will increase 
- Look at the hash rate 
- Indication of electricity measure the power that you draw per block that you mine 
- What to mine.com 
- Check algorithm (if merged mined you can compare)
- Algorithms will expend different power 
- You want better revenue per wattage 
- Myriad mining, mainly after Monero 
- GPU power
- Check balance on a power level 
- Blake Blake ASICs not working 
- Race with CPU 
- Merged mining Myriad- 

## Question 

What is the cost to control the network?

### Definition of Control 

Blocks for an attack? Reason for choosing a specific number of blocks?
When we use the word 'control' what is actual meant is the chance of mining $n$ number of blocks in a row to a certain threshold. What is the threshold?
In answering the question, what is $n$, when considering reorgs, they go passed the coinable transaction, that is a good limit. 

So to rephrase the question, what is the chance of mining $n$ blocks in a row?

A series of scenarios will be played out. Which scenario is more efficient? Which is cheaper- buying hashrate is easier?

### Definition of Cost 

### Assumptions 

- Assume the system is in equilibrium 
- Model is steady state
- Define cost that is agnostic of hashrate 
- Hashrate is constant --> Difficulty is constant 



### Input assumptions 

### Method

Monte Carlo Simulation 

$n/1000000 = p$

5? random generator to simulate PoW (allocate hashrate)

#### Scenario 1 

We control some fraction of the Tari merge mined hashrate greater than 50%.  

$n$ hashes mining Tari, you need more --> argue the cost is zero  

#### Scenario 2 

Merged mining  50% 		PoW 50% 
How much of the PoW hashrate do you need to buy control to make above statement true 

#### Scenario 3

1 x MM 33% 		2 x PoW 33% 33%

(Thought as a bad idea, flick between the 2- what would happen as they jump between each PoW)

#### Scenario 4

2 x MM

#### Scenario 5 

2 x MM 1 x PoW


### Hypothesis

Scenario 5 best, better than 2 last 3 

#### Version 2 

Consider the dynamic aspects of the hashrate. Scale for Myriad. 
Is the block time affected by sudden increase in hash rate. This is a dynamic problem. 

## Game Theory 

### PoW

Bitcoin is a digital currency which was introduced in 2009. Its security is based on a proof of work, and a transaction is only considered valid once the system obtains proof that a sufficient amount of computational work has been exerted by authorising nodes. The miners constantly try to solve cryptographic puzzles puzzles in the form of a hash computation. The process of adding a new block to the blockchain is called mining and these blocks contain a set of transactions. The average time to create a new block in blockchain is ten minutes. Two types of agents participate in the Bitcoin network: miners, who validate transactions and clients, who trade in currency. The blockchain is a shared data structure responsible for storing all transaction history. The blocks are connected with each other in the form of a chain. The first block of the chain is known as Genesis. Each block consists of a Block Header, Transaction Counter and Transaction. 

Each block in the chain is identified by a hash in the header. The hash is unique and generated bu the Secure Hash Algorithm (SHA-256). SHA takes any size plaintext and calculates a fixed size 256-bit cryptographic hash. Each header contains the address of the previous block in the chain. The process of adding blocks in the blockchain is called "mining of blocks". If miners mine a valid block 


### Mining 

Bitcoin is a decentralized cryptocurrency payment system, working without a single administrator or a third party bank. A bitcoin is created by miners, using complex mathematical "proof of work" procedure by computing hashes. For each successful attempt, miners get rewards in terms of bitcoin and transaction fees. Miners participate in mining to get this reward as income. Mining of cryptocurrency such as bitcoin becomes a common interest among the miners as the bitcoin market value is very high. As a side effect of this mining process, a lot of electricity is used in it.  

### Electricity 

Electricity is a semi-renewable resource, depending on the type of resource used for its production. Nevertheless, electricity plays an essential role in the bitcoin mining process since the whole mining process is based on it. The electricity consumed by the mining system is directly proportional to the computational power of that system. Moreover, powerful computers that specially designed fro bitcoin mining process, consumes much more electricity than the regular computers. 
