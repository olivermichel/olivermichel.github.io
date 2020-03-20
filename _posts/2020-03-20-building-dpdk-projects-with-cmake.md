---
layout: post
title: Building DPDK Projects with CMake
tags: [dpdk, cmake]
---

Intel's Data Plane Development Kit (DPDK) is a comprehnsive and powerful framework to build high
performance networked applications. Unfortunately, getting started with DPDK development can be
daunting. The Makefiles that come with the example applications seem complex and make several
assumptions about where your project resides. Additionally, many modern C and C++ applications
are built using the CMake build system. In this post I show how to simple it can be to integrate
DPDK in your existing CMake project. This is the first post in a series about DPDK development.

<!--more-->
