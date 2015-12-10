---
layout: page
permalink: /research/
---

## Defragmenting the Cloud
Network virtualization is a widely used technique to overcome the
ossification of networks. Being commonly applied in both datacenter as well
as wide-area settings, network virtualization enhances network flexibility
and enables innovation by making it easier to provide network
programmability. However, mapping virtual resources (links and nodes) to
physical (substrate) resources is a challenging problem and commonly
referred to as the provably NP-hard virtual network embedding (VNE) problem.
As virtual networks come and go over time, VNE algorithms tend to introduce
resource fragmentation in the network leading to request rejection when
resources would technically be available but cannot be assigned to the
requested topology or other request constraints. In this project we aim at
(1) improving VNE algorithms by considering resource fragmentation, (2)
design a defragmentation algorithm enabling the online reconfiguration of
virtual networks to reduce fragmentation. In a second step, we investigate
systems primitives to allow for reconfiguration of virtual networks. This
work is based on the work on Live Migration of Ensembles (LIME) as
presented by our group at HotNets-XI and SoCC '14.


## Policy Routing using Process-Level Identifiers
Enforcing and routing based on network-wide policies remains a crucial
challenge in the operation of large-scale enterprise and datacenter
networks. As current dataplane devices solely rely on layer 2 -- layer 4
identifiers to make forwarding decisions, there is no notion of the exact
origin of a packet in terms of the sending user or process. In this project
we ask the question: \emph{Can we go beyond the MAC?} That is, can
fine-grained process-level information like user ids, process ids or a
cryptographic hash of the sending executable be semantically used to make
forwarding decisions within the network? We designed a system architecture
and implemented an early prototype leveraging the P4 technology for
protocol-independent packet processing and forwarding in conjunction with
on-board tools of the Linux operating system. Using this system we are able
to make forwarding decisions within the network based on fine-grained
process-level identifiers that are traditionally only available within a
host's operating system.

## Network Abstractions in the Application Layer
Many of todays applications (in particular data processing applications)
use intra-application networks to connect computing elements. By making
intra-application networks part of the network itself, we simplify
applications by providing an abstraction of the network, freeing
applications from the responsibility of maintaining their own internal
topology management and forwarding systems. Also, moving the network edge
into the applications allows the network management to leverage advances
such as software-defined networking, providing a unified management across
an entire path. For these networks we are inspecting a new interface to the
network based on intra-application channels told to the network rather than
addresses.

## SDN Controller Architecture
While there is a broad variety of SDN controllers (both proprietary and
open source) available, we investigate the commonalities between SDN
controllers (often referred to as the network operating system) and
traditional operating systems. We believe network application should be
developed against an API that is similar to that of existing operating
systems. That is that SDN applications should run independently from each
other and not in a monolithic design (like today’s controllers suggest it).
Also applications should be able take advantage of features that operating
systems already provide (such as access control and process management). In
this area I am particularly interested in how such independent applications
are composed and are granted access to the network configuration.

## Low Latency Networking
Latency is an extremely important quality metric of computer networks.
While network hardware can be designed and provisioned to provide low
latency on average, heavy tails are pervasive in latency distributions of
almost all classes of networks due to a variety of reasons. We investigate
several techniques how to reduce this latency tail and provide networking
at the speed of light with a more uniform latency distribution compared to
what today’s networks are able to achieve. Strategies such as redundant
multi- or single-path routing, as well as adaptive source routing across
wide-area networks showed extremely satisfactory early results.
