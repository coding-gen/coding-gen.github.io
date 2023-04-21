---
layout: post
title:  "SingleStore Database Architecture"
date:   2021-05-11 15:00:44 -0800
tags: Databases
---

A training on internal architecture of the SingleStore database.

At SingleStore, I created an internal training to familiarize new hires in Customer Success with the major features of SingleStore database software. In this public training linked here, I go over a portion of the slides from that training, and demonstrate each of those components and how you can view and interact with them on a live cluster. In particular I show how data is partitioned and where it is stored in the cluster, demonstrating the shared-nothing architechture of SingleStore. This includes an example of how to create each supported table type, the differences in how they are stored, how memory management is exposed for monitoring, differences in aggregator types, common node file structures, as well as how to avoid common issues in creating test tables with dummy data.

[Check out my training video on YouTube](https://www.youtube.com/watch?v=FgNWb9Wkxf8)

For more information on SingleStore, see: [singlestore.com](https://www.singlestore.com)