---
description: This section covers all questions regarding V6 nodes
---

# Why does V6 require 50k TRAC?

### Running a node prior to V6 required 3k TRAC. Why does a V6 node require 50k TRAC ?

There are multiple reasons as to why the initial stake has been revised upwards.&#x20;

{% hint style="info" %}
First and foremost, running a full node now comes with a much greater responsibility both in terms of **persisting the public DKG state** and **providing a high quality of service** to asset publishers.
{% endhint %}

Prior to V5, the model to discourage bad behaviour by Data Holders (node runners) was to collaterize the same amount as the Data Creator for the duration of the job. In other words, the node runner would be punished by completely losing their collateral if they failed a litigation check.&#x20;

{% hint style="success" %}
This V5 litigation model does not require a high initial stake because bad behaviour punishment is completely unrelated. The deterrent to bad practices is solely related to the loss of the collateral amount for a given job, ranging from as little as 0.2 to 0.5 TRAC. This litigation process has nothing to do with the initial stake.
{% endhint %}

V6 introduces a new mechanism called **stake slashing** - a mechanism designed to discourage malicious behaviour and to incentivize good behaviour, network participation and availability. This is a significant change from a litigation model to a slashing model.&#x20;

{% hint style="success" %}
V6 stake slashing locks a percentage of the initial stake for a set duration. The initial stake therefore becomes a much more significant factor to penalize bad behaviours, inactivity or dishonest nodes. For example, a 5% slash to a 3k node is only 150 TRAC, whereas a 5% slash of a 50k node is 2500 TRAC! The higher the initial stake, the greater the slashing. Therefore, the slashing model is directly influenced by the initial stake, as opposed to the V5 litigation model.&#x20;
{% endhint %}

Stake slashing is also commonly used on the [Polkadot network](https://wiki.polkadot.network/docs/learn-staking#slashing) as well as [ETH2](https://www.blocknative.com/blog/an-ethereum-stakers-guide-to-slashing-other-penalties) and can vary from one protocol to another. The principle of locking tokens for misbehaviour and a higher initial stake (thus a higher barrier for entry), however, remains the same. For example, ETH2 requires 32 ETH to run a full node, and most ETH holders are expected to delegate their coins rather than run a full node. A similar pattern should be observed on OT Parachain once V6 goes live. In V5, the amount of nodes were too high for the amount of jobs on the network and a lot of nodes were also poorly maintained. A higher node collateral alongside a new slashing mechanism should serve as a deterrent to bad behaviour and incentivize good actors bringing a higher quality of service to the network. Nonetheless, in comparison to V5, the penalty for misbehaviour is a lot less punishing. The slashed tokens are to be returned to the full node runner at the end of the slash period, while a failed litigation in V5 would result in a complete loss of your collateral.&#x20;

|   Network users  |                                         Litigation                                        |                                                 Stake Slashing                                                 |
| :--------------: | :---------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------: |
|    Node Runner   | <p><strong>NEGATIVE</strong></p><p>Failed litigation leads to complete loss of tokens</p> | <p><strong>POSITIVE</strong></p><p>Slashing leads to tokens locked for a period of time without token loss</p> |
| Asset Publishers |     <p><strong>POSITIVE</strong> </p><p>Litigation is a deterrent to bad behaviour</p>    |                 <p><strong>POSITIVE</strong></p><p>Slashing is a deterrent to bad behaviour</p>                |
|    Delegators    |                 <p><strong>NEGATIVE</strong><br>No delegators possible</p>                |  <p><strong>POSITIVE</strong><br><strong></strong>Delegating is possible and share the same slashing risk</p>  |
|   TRAC Holders   |                 <p><strong>NEGATIVE</strong></p><p>Less token lock-up</p>                 |                             <p><strong>POSITIVE</strong><br>More token lock-up</p>                             |

Another factor in favor of a higher initial stake is to prevent a kind of "**Sybil attack**" - a single entity having control of multiple nodes in the network and establishing control of a significant portion of the network. The team has deemed that **technical decentralization** has been achieved with as little as 2000 nodes in the network, and 50k per node is the optimal value between enabling large number of nodes, while also making it hard to control a significant portion of the network.&#x20;

{% hint style="success" %}
In short, the higher node collateral amount serves as a crucial **network security component** as well as an **insurance for quality of service** of the network.&#x20;

The minimum stake can be amended in the future based on network activity and will be proposed in a RFC.&#x20;
{% endhint %}
