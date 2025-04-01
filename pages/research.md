---
layout: page
permalink: /research/
---

## Vision

As a systems and networking researcher, my works focuses on improving the performance and scalability of *emerging networked applications*, in the face of their rapid growth, complexity, and associated resource overheads.
Due to this complexity, achieving this goal warrants a holistic cross-layer approach where I cover the entire stack, from the physical layer to the higher-layer intricacies of rich, user-facing applications.
My research takes a unique measurement-driven approach that emphasizes on understanding the operation and performance of applications *in the wild* and *across layers* by  designing measurement methodologies and building measurement systems before crafting practical measurement studies that provide unique insight into actual deployments of large-scale systems.
I use these insights to address problems across the stack by designing and building systems that leverage advances in network programmability to improve Quality of Experience (QoE) for users while simplifying and reducing overheads of running these systems for operators.


## Current Projects

**Improving the Scalability of Video-Conferencing Infrastructure** --- My work on video conferencing started with enabling visibility into the increasingly important area of real-time communications, which also includes, for example, live streaming and cloud gaming. These systems have stringent performance and scalability requirements which are often hard to meet in today's networks and using today's implementations. Specifically, we found that this workload is inherently hard to scale as the amount of packets to process grows quadratically with meeting size and under-provisioning of these servers has direct impact on QoE. Our analysis of Zoom, however, also revealed that forwarding and adapting media signals in video conferencing is strikingly similar to traditional packet processing.
Based on this insight and following a long line of work on software-defined networking (SDN), we show how to rearchitect video-conferencing systems and offload all media forwarding to an efficient data plane which runs on line-rate programmable switches, increasing throughput by up to 200 times while reducing latency 26 times. [[arXiv '25](/publications)]

**Boosting the Performance of Real-Time Communication Systems over 5G Networks** --- Rapid delay variations in today's wireless networks impair the QoE of low-latency, interactive applications, such as video conferencing and AR/VR. Our measurements have revealed that applications essentially operate in the dark as it is hard to differentiate between short-term delay artifacts stemming from wireless scheduling and retransmissions and those caused by congestion. To tackle this problem, we built Athena, a framework that correlates high-resolution measurements across Layer 1 to Layer 7 to remove the fog from the window through which today's congestion-control algorithms see the network. Athena extracts 5G control-channel telemetry of physical-layer data units, retransmissions, and scheduling decisions and precisely time-synchronizes these measurements with packets at the network layer and video frames or audio samples at the application layer. As a result, Athena can identify the cause of distorted audio or stuttering video and feed this information back to the applications. This cross-layer view of the network empowers the networking community to revisit and re-evaluate scheduling and congestion-control algorithms in light of the complex, heterogeneous networks that are in use today, paving the way for network-aware applications and application-aware networks. [[HotNets '24](/publications)]

## Previous Projects

**Monitoring and Improving Video-conferencing Sessions in the Data Plane** --- Video-conferencing applications, such as Google Meet, Microsoft Teams, and Zoom, have gained popularity over the past several years. These applications are sensitive to network delay and data-intensive as they use high-quality webcam and audio streams. As a result, small changes in the underlying network conditions can have a significant impact on the user-perceived quality of an online meeting. Reduced network bandwidth results in poor audio or video quality or even frozen pictures; increased network delay results in lag which can make conversations difficult. In this project, we aim to understand how the network impacts the quality and performance of video-conferencing sessions in the wild and how modern programmable network devices can be leveraged to improve the quality of experience (QoE) of such applications. We are particularly interested in developing techniques to monitor the quality of video conferences as they take place, answer why a performance anomaly is occurring, and, subsequently, reconfigure the network or apply custom packet processing logic that improves meeting quality in real time.

**Next-Generation Network Telemetry and Analytics** --- Traditionally, network monitoring
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

**Defragmenting the Cloud** ---	Network virtualization is an extensively used approach to allow multiple tenants with different network architectures and services to coexist on a shared data center infrastructure. Core to its realization is the mapping (or embedding) of virtual networks onto the underlying substrate infrastructure. Existing approaches are not suitable for cloud environments as they lack its most fundamental requirement: elasticity. To address this issue, we introduce two new network primitives – expand and contract – which allow virtual networks to scale up and down. Mapping and scaling virtual networks over time, however, introduces fragmentation in the substrate network. This is akin to fragmentation in a file system where files are not laid out in contiguous physical blocks of the storage device. We define metrics for fragmentation and show that this problem not only negatively impacts the revenue of the data center provider as the virtual network acceptance rate decreases, but also profoundly impacts network performance and reliability for tenants and their applications.

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
