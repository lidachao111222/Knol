---
description: Casper Proof of Stake (权益证明) 研究汇编
---

# Casper PoS

## 什么是 Proof of Stake \(权益证明\)？

**权益证明（PoS）是一种用于公共区块链的共识算法，该算法取决于验证者在网络中的经济权益。**在基于工作量证明（PoW）的公共区块链（例如目前的比特币和以太坊）中，通过奖励解决密码难题的参与者，以验证交易并创建新区块（即挖矿）。而在基于 PoS 的公共区块链（以太坊即将发布的 Casper）中，一组验证者轮流对下一个区块进行提议和投票，每个验证者的投票权重取决于其押金（即权益）的多少。 PoS 的显着优势包括**提高安全性、降低中心化风险和节省能耗**。

通常，权益证明算法是这样运行的：区块链持续追踪一个验证者集合，任何持有区块链基础加密货币（以太坊为 ETH）的人都可以通过**发送一种特殊的交易将其  ETH 锁定为押金**，以成为验证者。然后，所有的验证者都可以通过参与共识算法完成新区块的创建并确认新区块的产生。

目前有许多种共识算法，对参与共识算法验证者的奖励机制也多种多样，因此，存在不同类别的权益证明机制。从算法角度来看，主要有两种类型：基于链的 PoS 和 BFT（拜占庭容错）风格的 PoS。

在**基于链的 PoS** 中，该算法在每个时隙（每10秒的时间段可能作为一个时隙）中伪随机地选择一个验证者，并向该验证者分配创建单个区块的权限，并且该区块必须指向某个先前的区块（按照最长链规则，通​​常是最长链末尾的区块），因此随着时间的推移，大多数区块会按照顺序组成一条不断延伸的链。

在**BFT（拜占庭容错）式的 PoS** 中，验证者被**随机分配**提议区块的权利，但是要就区块有效性达成一致需要通过多轮回合制过程，即每个验证者在每一回合中针对某个特定区块投票，从而就区块的规范性达成共识。在该过程结束时，所有（诚实的和在线的）验证者都将商定是否有任何给定区块被纳入链中，其结果是永久有效的。需要注意的是，区块仍然可以链接在一起，关键区别在于，对某个区块达成的共识将保留在区块内，而不取决于其后链的长度或大小。

更多相关信息参见：[PoS F](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ)[AQs](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ).
