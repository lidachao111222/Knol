# 以太币 Ether

## 概述

Ether（又写作ETH或Ξ），中文译作以太币，是用于以太坊网络的原生加密货币，并为维护交易安全的矿工提供奖励。以太坊计划在2019-2021年对协议进行升级，将以计算成本较低的PoS（权益证明）机制代替工作量证明挖矿，网络安全将由验证者维护，他们也将按一定比例获得奖励。Ether当前还具有许多用例，例如价值储藏（例如贷款抵押）、交换媒介（例如贸易和支付情境）以及价值尺度（应用于数字货币市场）。

## 以太币用例

### 网络用例 🛠 

要在以太坊网络中进行交易，以太币是不可或缺的。

如[gas部分](https://docs.ethhub.io/using-ethereum/transactions/#gas)所述，网络中发生的每笔交易都需要一定数量的gas，gas是用于度量处理交易所需计算能力的单位。矿工要付出算力成本处理交易并将其打包在区块中，理应获得相应的补偿。在以太坊系统中，这就要通过在每次交易中设定gas价格来完成，gas以Gwei（1 ETH = 1,000,000,000 Gwei）作为单位。

举个例子：用户将ETH从一个帐户发送到另一个帐户需要花费21,000 gas，如果将gas价格定为1 Gwei，则此交易花费0.000021 ETH。

### 价值储藏 💰 

以太币作为以太坊网络的原生货币，其价值源于众多不同的因素。在以太坊网络中，我们可以使用以太币来执行一系列功能，其中包括：

用于支付以太坊交易费用（以gas的形式）；用作各种去中心化金融应用的抵押（如MakerDAO，Compound）；可以借出或借用（Dharma）；用作被某些零售商和服务提供商认可的支付方式；用作交换媒介，以购买基于以太坊的通证（通过ICO或交易所）、加密收藏品、游戏内物品以及其他非同质化通证（NFT，Non-fungible Token）；或是作为完成任务的赏金奖励 \(Gitcoin, Bounties Network\)。

此外，在以太坊2.0（Serenity）中，用户将能够成为验证者，每个验证者通过提供计算资源并锁定32个以太币来为网络安全保驾护航。因此，预计PoS（权益证明）机制将锁定大量的流通中以太币。目前也在进行关于引入“fee-burn”（手续费销毁）机制的讨论，在该机制中，用于支付交易费用的部分以太币将被“销毁”，从而减少流通中的以太币供应量。

除了以上这些实用性价值，ETH还具有一定投机价值，也即通过投机活动\(比如交易和投资行为\)而获得的价值，这些投机活动构成了当前整个加密货币领域的主要价值来源。我们知道，2017年的熊市激发了大规模的投机热潮，有些加密资产的价格在短短几个月就上涨了超过1000倍。人们的投机心理往往能够为加密生态系统引入新的资金，而这些资金能够被用于投资不同项目。但这种投机行为可能会损害所有加密资产的短期市场情绪。

> 以太坊中的其他通证可以代替ETH吗？

从理论上来说是可行的，但从实际上来说不可以！这种使用非ETH资产来维护以太坊网络的概念被以太坊社区称作“经济抽象化”\(Economic Abstraction\)。社区认为，经济抽象化问题将使得矿工/验证者在把有效交易打包到区块时，将接受除了ETH以外的其他通证作为手续费。

但实际上，以太坊协议不太可能实行经济抽象化，因为经济抽象化将导致ETH贬值，而这将会损害整个以太坊区块链的安全性。

> 那么具有价值的ETH如何保障以太坊网络的安全？

在PoW\(工作量证明\)系统中，矿工们会竞相计算出新区块，以此来获得相应的奖励\(获得某个区块链协议的原生加密资产，以太坊网络中即ETH\)。随着该原生加密资产价格的上涨，自然可以吸引更多的矿工加入进来，而矿工数量增加也就意味着挖矿难度将相应提升。随着网络的挖矿难度增加，个人矿工要挖出一个新区块将越来越难，从而便催生出了大规模的挖矿作业，也即所谓的矿场\(mining farms\)，这是当前的PoW 网络（前提是达到一定规模）中常见的一种有利可图的挖矿方式。矿工也可以加入“矿池”，以此来提高他们挖出新区块并获得相应奖励的几率。

当前，不管是对于个人还是组织来说，要成功地对比特币或以太坊PoW区块链发起攻击或者获得整条链的控制权，都需要花费巨额的资金成本。

以太坊在Serenity阶段过渡到PoS\(权益证明\)机制时，用户将通过抵押32枚ETH成为验证者，然后通过验证区块来获得额外的ETH奖励，验证者奖励将遵循一个动态的奖励发行率。

在PoS机制中，攻击以太坊网络的成本将与所耗费的ETH成本挂钩。不同于PoW机制中的能源密集型挖矿方式，PoS机制中的验证者需要先“抵押”ETH，假如其试图进行欺诈行为，将会因此损失部分或全部所抵押的ETH。在以太坊2.0网络中抵押ETH的验证者数量越多，网络就越安全，因为攻击者要实施攻击行为就需要购买更多的ETH作为成本。而且，在攻击者不断购入大量ETH时，ETH的价格很可能迅速上涨，因此攻击成本会高得难以负担。

### 交换媒介 ⚖ 

在经济体系中，某种事物想要充当货币的职能，则需要充当良好的交换媒介\(MoE\)、价值尺度\(UoA\)和价值储藏手段\(SoV\)。首先，在当前的以太坊经济体系中，ETH 为很多DApp\(去中心化应用\)充当了交换媒介，因为DApp的提供商接受用户使用ETH来交换其他同质/非同质通证以及服务。其次，许多组织也将ETH视为价值尺度\(比如通过ICO方式筹集ETH\)。最后，ETH一直以来都作为一种价值储藏手段，由于ETH的稀缺性、供应增长的可预测性以及固有的实用性，很多投资人和投机者出于投资目的购买并持有ETH。

无论是实体还是数字形式，该事物通常必须具有五种不同的基本属性，才能被视作货币：即便携性、耐用性、可分性、可替代性、已存在历史\(基于[林迪效应](https://en.wikipedia.org/wiki/Lindy_effect)，即对于一些不会自然消亡的事物，例如一种技术、一个想法，其预期寿命和目前已经存在的时间成正比\)。从这个角度来看，ETH具有高度的便携性\(数字形式\)、耐用性\(数字形式\)、可分性\(最多可分成0.00000001个ETH\)，但ETH虽然可以与其他通证种类进行置换，但用户的账户/地址很容易被列入黑名单，因此ETH的可替代性受限，但诸如zk-SNARKs（零知识证明）等隐私保护协议将最终解决以太坊的这一问题。

以太坊网络自2015年开始运行，并持续构建着自身的强大历史。在其既往历史中，以太坊网络以及ETH按照99.99%的预期正常运转着，另外的0.01%则包含了The DAO分叉、一些大型的智能合约攻击、多个协议层漏洞、上海DoS攻击等事件，还经历了来自加密货币社区的负面评论和几次熊市。

此外，ETH 还具有额外的属性，比如抗审查性、去信任化、匿名性，以及与其他加密网络的互操作性。

一直以来，加密资产的供应机制普遍会引起社区各方的激烈争论\(尤其是在比特币社区中\)，当前的加密货币供应机制有两种主要方式：限额供应\(如比特币\)和可预计的、难以改变的低发行率\(以太坊2.0计划如此\)。

在以太坊2.0阶段（即实现了分片和PoS），尽管低通胀率能始终保证验证者维护以太坊网络安全的行为获得奖励，但对于非验证者的普通用户来说，低通胀率将可能会削弱ETH的价值\(注：价值≠价格\)。尽管由于上面提到的种种原因（验证者对流通中的部分ETH进行抵押，各类金融应用也占据了一部分ETH，作为交易费的ETH还有可能面临销毁），流通中的ETH数量将会有所减少，从而人们能获取的ETH也会减少，而这在一定程度上抵消了低通胀率带来的ETH贬值问题。

## 参考资源

* [EthHub：What is Ether？](https://docs.ethhub.io/ethereum-basics/what-is-ether/)
* [Why Ether is Valuable](https://medium.com/ethhub/why-ether-is-valuable-2b4e39e01eb3)
* [Ether: A New Model for Money](https://medium.com/pov-crypto/ether-a-new-model-for-money-17365b5535ba)

