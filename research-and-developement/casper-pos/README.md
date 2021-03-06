---
description: Casper Proof of Stake (权益证明) 研究汇编
---

# Casper PoS

## 什么是 Proof of Stake \(权益证明\)？

**权益证明（PoS）是一种用于公共区块链的共识算法，该算法取决于验证者在网络中的经济权益。**在基于工作量证明（PoW）的公共区块链（例如目前的比特币和以太坊）中，通过奖励解决密码难题的参与者，以验证交易并创建新区块（即挖矿）。而在基于 PoS 的公共区块链（以太坊即将发布的 Casper）中，一组验证者轮流对下一个区块进行提议和投票，每个验证者的投票权重取决于其押金（即权益）的多少。 PoS 的显着优势包括**提高安全性、降低中心化风险和节省能耗**。

通常，权益证明算法是这样运行的：区块链持续追踪一个验证者集合，任何持有区块链基础加密货币（以太坊为 ETH）的人都可以通过**发送一种特殊的交易将其  ETH 锁定为押金**，以成为验证者。然后，所有的验证者都可以通过参与共识算法完成新区块的创建并确认新区块的产生。

目前有许多种共识算法，对参与共识算法验证者的奖励机制也多种多样，因此，存在不同类别的权益证明机制。从算法角度来看，PoS主要有**两种**类型：基于链的 PoS 和基于BFT（拜占庭容错）的PoS。

在**基于链的 PoS** 中，该算法在每个时隙（每10秒的时间段可能作为一个时隙）中伪随机地选择一个验证者，并向该验证者分配创建单个区块的权限，并且该区块必须指向某个先前的区块（按照最长链规则，通​​常是最长链末尾的区块），因此随着时间的推移，大多数区块会按照顺序组成一条不断延伸的链。

在**基于BFT（拜占庭容错）的 PoS** 中，验证者被**随机分配**提议区块的权利，但是要就区块有效性达成一致需要通过多轮回合制过程，即每个验证者在每一回合中针对某个特定区块投票，从而就区块的规范性达成共识。在该过程结束时，所有（诚实的和在线的）验证者都将商定是否有任何给定区块被纳入链中，其结果是永久有效的。需要注意的是，区块仍然可以链接在一起，关键区别在于，对某个区块达成的共识将保留在区块内，而不取决于其后链的长度或大小。

## PoS vs. PoW 

* 不需要消耗大量的电力来保证区块链的安全。（据估计，作为共识机制的一部分，以太坊和比特币每天消耗的电力和硬件成本超过一百万美元）
* 不再需要消耗高额电力，也就意味着不需要增发大量代币来激励参与者持续参与到网络中。理论上，PoS机制下甚至有可能出现负值净发行量，因为部分交易费会被“销毁”，供应量随着时间慢慢减少。
* PoS催生出许多基于博弈论的各种不同技术，这些技术能更有效地抑制中心化卡特尔组织的形成。如此一下，就能阻止中心化对网络造成损害（比如在PoW机制下的自私挖矿）
* 如果规模经济难以形成，那么中心化的风险也降低了。一千万美元的投入会比一百万美元的投入给你带来高出十倍的回报，而没有任何额外的不成比例的收益，因为可以针对大规模挖矿设备进行大量投资，这是PoW机制的一种优势所在。
* PoS机制能够对各种形式的51%攻击施以比PoW更重的经济惩罚。用Vlad Zamfir的话来说就是“如果你参与了51%攻击，那你的损失无异于ASIC矿场被焚毁。”

#### 51％攻击

51%攻击的四种基本类型：

* 确定性回滚：已经敲定了区块A的验证者随后敲定某个竞争区块A’，从而破坏了区块链的确定性保证
* 敲定无效区块：验证者敲定一个无效的（或不可用的）区块。
* 活性拒绝：验证者停止敲定区块。
* 审查：验证者阻止部分或所有交易，或阻止区块被纳入链中。

在第一种情况，用户可以在带外协商哪个被敲定的区块最先出现就选择哪个区块。第二种情况可以利用欺诈证明和数据可用性证明来解决。第三种情况可以通过修改PoS算法来解决，即如果验证者不参与到共识中的话，该算法会在逐渐减少（“泄漏”）未参与节点在验证者集合中的权重。Casper FFG论文中有对此种情况进行说明。

第四种情况是最难解决的。第四种情况能通过“少数派软分叉”来修复，如果少数诚实验证者一致认为其余大多数验证者在对他们进行审查，于是便停止在当前的链上创建区块。继而，他们继续搭建自己的链，并最终通过上文提到的“泄漏”机制来确保这些诚实的少数验证者成为新链上的2/3绝大多数。到那时，市场会倾向于支持由诚实节点控制的链。

## Staking常见问题

#### 我为什么想质押我的ETH？ <a id="why-would-i-want-to-stake-my-eth"></a>

因为质押ETH并证明正确区块的话，根据一定网络收益率，你将获得额外的ETH奖励和部分网络交易费。点击[这里](https://docs.ethhub.io/ethereum-roadmap/ethereum-2.0/eth-2.0-economics)查看详情。

#### 质押的最低要求是什么？ <a id="what-are-the-minimum-requirements-to-stake"></a>

* 每个验证者至少质押32ETH
* 计算机的硬件配置符合条件
* 网络连接

#### 质押需要运行哪些软件？ <a id="what-software-do-i-need-to-run-to-stake"></a>

考虑在以太坊上进行质押时，需要了解两类主要软件：

* 信标节点：这是你所运行的验证者的中心枢纽
* 储存有效的状态、处理与对等节点和输入的同步、广播区块和证明。
* 有一个客户端可以连接的gRPC服务器并提供一个公共API。
* 验证者客户端：与你的信标节点通信并进行区块签名。你可以运行多个验证者客户端，每32 ETH能够激活一个。
* 储存重要的私密信息，比如RANDAO reveal、共享数据的托管证明和BLS私钥。
* 能高效切换底层信标链节点。
* 追踪共享状态的执行数据和验证者已签名的数据块。

这意味着可以运行三种软件组合：

1. 仅运行信标节点
2. 信标节点 + 验证者客户端
3. 信标节点 + 多个验证者客户端

#### 运行这些软件对硬件设备有什么要求？ <a id="what-are-the-hardware-requirements-to-run-this-software"></a>

待定中。理想情况下，我们可以将上述三种组合对设备的要求降到最低。

#### 在Staking过程中断网了会怎么样？ <a id="what-happens-if-i-lose-my-internet-connection-while-staking"></a>

成为验证者的关键在于确定你能持续对区块进行投票，从而达到维护网络安全的目的。因此，在任何时候如果某个验证者客户端离线了，为了激励验证者保持在线，离线验证者将会面临轻微的惩罚。这种情况会有两种情境：

1. 如果在敲定区块时离线，离线验证者会在一年内会失去押金的x%，x=当前利率
2.  例如，如果当前利率为5%，离线验证者每天将失去押金的0.0137%，但如果保持在线的话这就会转化成同等的收益。
3. 如果区块不是在敲定期间（大于33%的验证者离线），那么离线验证者会在18天内失去押金

   的60%。

如果验证者押金低于16ETH，将被完全移除出验证者集。

#### 如果我参与Staking的话，我的ETH会被锁定多久？ <a id="how-long-is-my-ether-locked-up-if-i-stake"></a>

如果想从验证者客户端提出ETH时，那么你会进入一个提款队列。如果没有队列的话，那么最短的赎回时间为18小时，时间会根据当时的提款人数进行动态调整。

## 延伸阅读

[PoS F](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ)[AQs](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ).

