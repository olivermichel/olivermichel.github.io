---
layout: page
permalink: /research/
---

## Current Projects

**Packet-Level Analytics in Software without Compromises** --- Traditionally, network monitoring
and analytics systems rely on aggregation (*e.g.,* flow records) or sampling to cope with high
packet rates. This has the downside that, in doing so, we lose data granularity and accuracy, and in
general limit the possible network analytics we can perform. Recent proposals leveraging
software-defined networking or programmable hardware provide more fine-grained, per-packet
monitoring but still are based on the fundamental principle of data reduction in the network, before
analytics. In this work, we provide a first step towards a cloud-scale, packet-level monitoring and
analytics system based on stream processing entirely in software. Software provides virtually
unlimited programmability and makes modern (*e.g.,* machine-learning) network analytics applications
possible. We identify unique features of network analytics applications which enable the
specialization of stream processing systems. As a result, an evaluation with our preliminary
implementation shows that we can scale up to several million packets per second per core and
together with load balancing and further optimizations, the vision of cloud-scale per-packet network
analytics is possible.

**Defragmenting the Cloud** ---	Network virtualization is an extensively used approach to allow
multiple tenants with different network architectures and services to coexist on a shared data
center infrastructure. Core to its realization is the mapping (or embedding) of virtual networks
onto the underlying substrate infrastructure. Existing approaches are not suitable for cloud
environments as they lack its most fundamental requirement: elasticity. To address this issue, we
introduce two new network primitives -- *expand* and *contract* -- which allow virtual networks to
scale up and down. Mapping and scaling virtual networks over time, however, introduces fragmentation
in the substrate network. This is akin to fragmentation in a file system where files are not laid
out in contiguous physical blocks of the storage device. We define metrics for fragmentation and
show that this problem not only negatively impacts the revenue of the data center provider as the
virtual network acceptance rate decreases, but also profoundly impacts network performance and
reliability for tenants and their applications. Instead of further improving embedding algorithms to
tackle this problem, in this work, we present a yet unexplored approach: leveraging network
migration techniques to *defragment* the network. We introduce network defragmentation as a new
management primitive and propose algorithms to materialize it. We show through extensive simulations
that our techniques significantly improve network performance while maintaining high utilization of
the infrastructure, thus increasing provider revenue. On average, using defragmentation leads to 20%
reduction in path length and utilization and cuts the number of very long paths (longer than half of
the network diameter) between 52% and 62%. Moreover, it doubles the number of servers utilized by
50% or less as a result of consolidating resource utilization.

## Previous Projects

**Policy Routing using Process-Level Identifiers** --- Enforcing and routing based on network-wide
policies remains a crucial challenge in the operation of large-scale enterprise and datacenter
networks. As current dataplane devices solely rely on layer 2 -- layer 4 identifiers to make
forwarding decisions, there is no notion of the exact origin of a packet in terms of the sending
user or process. In this project we ask the question: *Can we go beyond the MAC?* That is, can
fine-grained process-level information like user ids, process ids or a cryptographic hash of the
sending executable be semantically used to make forwarding decisions within the network? We designed
a system architecture and implemented an early prototype leveraging the P4 technology for
protocol-independent packet processing and forwarding in conjunction with on-board tools of the
Linux operating system. Using this system we are able to make forwarding decisions within the
network based on fine-grained process-level identifiers that are traditionally only available within
a host's operating system.

**Network Abstractions in the Application Layer** --- Many of todays applications (in particular
data processing applications) use intra-application networks to connect computing elements. By
making intra-application networks part of the network itself, we simplify applications by providing
an abstraction of the network, freeing applications from the responsibility of maintaining their own
internal topology management and forwarding systems. Also, moving the network edge into the
applications allows the network management to leverage advances such as software-defined networking,
providing a unified management across an entire path. For these networks we are inspecting a new
interface to the network based on intra-application channels told to the network rather than
addresses.

**SDN Controller Architecture** --- While there is a broad variety of SDN controllers (both
proprietary and open source) available, we investigate the commonalities between SDN controllers
(often referred to as the network operating system) and traditional operating systems. We believe
network application should be developed against an API that is similar to that of existing
operating systems. That is that SDN applications should run independently from each other and not
in a monolithic design (like today’s controllers suggest it). Also applications should be able take
advantage of features that operating systems already provide (such as access control and process
management). In this area I am particularly interested in how such independent applications are
composed and are granted access to the network configuration.

**Low Latency Networking** --- Latency is an extremely important quality metric of computer
networks. While network hardware can be designed and provisioned to provide low latency on average,
heavy tails are pervasive in latency distributions of almost all classes of networks due to a
variety of reasons. We investigate several techniques how to reduce this latency tail and provide
networking at the speed of light with a more uniform latency distribution compared to what today’s
networks are able to achieve. Strategies such as redundant multi- or single-path routing, as well
as adaptive source routing across wide-area networks showed extremely satisfactory early results.
