---
 layout: post
 title: distribute
---
 
原文链接：https://leetcode.com/discuss/general-discussion/1105898/System-Design%3A-Introduction-to-Distributed-Systems-or-Designing-a-highly-available-system 
 
什么是分布式系统？
   多个实体通过网络形成的一个互相联接的系统。
   每个实体（单元）可以被认为是图中的一个节点。每个节点可以很快的执行在自己节点上的操作，但是节点直接的互相交流不一定快
 
 ##### 分布是系统的目标
 ###### 透明性（transparency): 用户不知道具体执行过程
 ###### 可扩展性（scalability): 系统的增长
 ###### 可用性 （availability): 系统的可用性，即用户能否按照正常使用系统。其中一个要素是系统的正常使用时间（uptime），系统的正常使用时间不取决任一节点的正常使用时间，而是由整个所有节点的正常使用时间所决定。 
 
 ##### CAP theorm
 ###### Partition 是指分布式系统中的交流中断--两个节点的联接的丢失或暂时的延迟，因为现实情况中，因为网络或者硬件的原因，中断无法避免。中断容忍性是必要的。
 ###### Consistency 是指连接任何节点的客户端在任一时刻看到的消息必须相同。要求对任一节点的写操作，必须完成之前，同时转发或者复制到系统中的所有的其他节点。
 ###### Availability 是指用户的所有请求必须得到回应，即便某个节点挂掉。
 ###### CAP理论是指分布式系统parttiotion发生时时，在系统一致性和可用性之间取舍。
