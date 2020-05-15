---
layout: post
title:  "Java Garbage Collection"
categories: [ java ]
tags: [java, featured]
image: https://i.ytimg.com/vi/UnaNQgzw4zY/maxresdefault.jpg
---

Garbage collectors have two possible collection types, incremental collection and full collection. Incremental collection is the better because it keeps running in the background, finding bits of objects to be garbage collected and does not require much systems resources and definitely does not halt the system.Parallel garbage collector on the other hand halts the system when it runs and uses the system's resources extensively.

So, most modern GCs (including G1) will try to ensure that the incremental collection will be enough and a full collection will never be required. However, if lots of objects are generated across the program/application it becomes necessary to run a Full garbage collection.

Presently, the G1 full collection implementation is only single threaded. So a 32 core server having 128GB memory will stop and pause until a single thread takes out the garbage. In Java 10 this has been improved to run in Parallel. This means that the Full GCs will be on multiple threads in parallel, still pausing the JVM’s progress whilst it completes. The number of threads can be optionally configured using -XX:ParallelGCThreads So on systems which support parallel execution, parallel G1GC is executed so that the time consumed is minimized. The GC can now run with all the resources we provide to it.