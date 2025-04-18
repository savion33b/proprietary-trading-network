<p align="center">
  <a href="https://taoshi.io">
    <img width="500" alt="taoshi - ptn repo logo" src="https://i.imgur.com/5hTsp97.png">
  </a>
</p>

<div align='center'>

[![Discord Chat](https://img.shields.io/discord/1163496128499683389.svg)](https://discord.gg/2XSw62p9Fj)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

</div>

<p align="center">
  <a href="https://taoshi.io">Website</a>
  ·
  <a href="#installation">Installation</a>
  ·  
  <a href="https://dashboard.taoshi.io/">Dashboard</a>
  ·
  <a href="https://twitter.com/taoshiio">Twitter</a>
    ·
  <a href="https://twitter.com/taoshiio">Bittensor</a>
</p>

---

<details>
  <summary>Table of contents</summary>
  <ol>
    <li><a href="#proprietary-trading-network">Proprietary Trading Network</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#how-does-it-work">How does it work?</a></li>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
    <li><a href="#building-a-model">Building A Model</a></li>
    <li><a href="#testing">Testing</a></li>
    <li><a href="#faq">FAQ</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>

  </ol>
</details>

--- 

<details id='bittensor'>
  <summary>What is Bittensor?</summary>

Bittensor is a mining network, similar to Bitcoin, that includes built-in incentives designed to encourage computers to provide access to machine learning models in an efficient and censorship-resistant manner. Bittensor is comprised of Subnets, Miners, and Validators.

> Explain Like I'm Five

Bittensor is an API that connects machine learning models and incentivizes correctness through the power of the blockchain.

### Subnets

Subnets are decentralized networks of machines that collaborate to train and serve machine learning models.

### Miners

Miners run machine learning models. They send signals to the Validators.

### Validators

Validators recieve trade signals from Miners. Validators ensure trades are valid, store them, and track portfolio returns. 

</details>

<br />
<br />

# Proprietary Trading Subnet

This repository contains the code for the Proprietary Trading Network (PTN) developed by Taoshi.

PTN receives signals from quant and deep learning machine learning trading systems to deliver the world's
most complete trading signals across a variety of asset classes.

# Features

🛠️&nbsp;Open Source Strategy Building Techniques (In Our Taoshi Community)<br>
🫰&nbsp;Signals From a Variety of Asset Classes - Forex, Indices, Crypto<br>
📈&nbsp;Higher Payouts<br>
📉&nbsp;Lower Registration Fees<br>
💪&nbsp;Superior Cryptocurrency Infrastructure<br>
🔎&nbsp;<a href="https://dashboard.taoshi.io/">Trading Visualization Dashboard</a>

## How does it work?

PTN is the most challenging & competitive network in the world. Our miners need to provide futures based signals (
long/short)
that are highly efficient and effective across various markets to compete (forex, crypto, indices). The top miners are
those that provide the most returns, while never exceeding certain drawdown limits.

### Rules

1. Miners can submit LONG, SHORT, or FLAT signal for Forex, Crypto, and Indices trade pairs into the network.
2. Orders outside of market hours are ignored. 
3. Miners can only open 1 position per trade pair/symbol at a time.
4. Positions are uni-directional. Meaning, if a position starts LONG (the first order it receives is LONG), 
it can't flip SHORT. If you try and have it flip SHORT (using more leverage SHORT than exists LONG) it will close out 
the position. You'll then need to open a second position which is SHORT with the difference.
5. Position leverage is bound per trade_pair. If an order would cause the position's leverage to exceed the boundary, the position leverage will be clamped.
6. You can take profit on an open position using LONG and SHORT. Say you have an open LONG position with .75x 
leverage and you want to reduce it to a .5x leverage position to start taking profit on it. You would send in a SHORT signal
of size .25x leverage to reduce the size of the position. LONG and SHORT signals can be thought of working in opposite 
directions in this way.
7. Miners can explicitly close out a position by sending in a FLAT signal. 
8. Miners are eliminated if they are detected as plagiarising other miners. (more info in  the "Eliminations" section).
9. There is a fee per trade pair position. The fee scales with leverage. e.x a 10x leveraged position will have a 10x higher fee.
10. There is a minimum registration fee of 5 TAO on the mainnet subnet.
11. There is an immunity period of 9 days to help miners submit orders to become competitive with existing miners. Eliminated miners do not benefit from being in the immunity period.
12. Based on portfolio metrics such as omega score and total portfolio return, weights/incentive get set to reward the best miners.

With this system only the world's best traders & deep learning / quant based trading systems can compete.


# Eliminations

In the Proprietary Trading Network, Eliminations occur for miners that commit Plagiarism.


### Plagiarism Eliminations

Miners who repeatedly copy another miner's trades will be eliminated. Our system analyzes the uniqueness of each submitted order. If an order is found to be a copy (plagiarized), it triggers the miner's elimination.

### Post-Elimination

After elimination, miners are not immediately deregistered from the network. They will undergo a waiting period, determined by registration timelines and the network's immunity policy, before official deregistration. Upon official deregistration, the miner forfeits registration fees paid.



# Get Started

### Mainnet Trade Dashboard
Take a look at the current competition <a href="https://dashboard.taoshi.io/">Dashboard</a>

### Validator Installation

Please see our [Validator Installation](https://github.com/taoshidev//proprietary-trading-network/blob/main/docs/validator.md) guide.

### Miner Installation

Please see our [Miner Installation](https://github.com/taoshidev/proprietary-trading-network/blob/main/docs/miner.md) guide.

# Building a strategy

We recommend joining our community hub via Discord to get assistance in building a trading strategy. We have partnerships with both Glassnode and LunarCrush who provide valuable data to be able to create an effective strategy. Analysis and information
on how to build a deep learning ML based strategy will continue to be discussed in an open manner by team Taoshi to help
guide miners to compete.

# Contributing

For instructions on how to contribute to Taoshi, see CONTRIBUTING.md and Taoshi's code of conduct.

# License

Refer to the <a href='?tab=MIT-1-ov-file'>License</a> page for information about Taoshi's licensing.

Bittensor's source code in this repository is licensed under the MIT License.
