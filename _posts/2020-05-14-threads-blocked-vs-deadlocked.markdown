---
layout: post
title:  "Threads: Deadlocked Vs Blocked"
categories: [ java ]
tags: [java, featured]
image: https://howtodoinjava.com/wp-content/uploads/2012/10/deadlock1.jpg
excerpt: "Learning about the difference between Deadlocked and Blocked states."
---


Many developers are confused between thread states - Deadlocked and Blocked.A thread is in the deadlocked state when Thread A is waiting for a lock which is acquired by Thread B and Thread B in return waits for a lock which is acquired by Thread A. 
This in turn makes a circular dependency andthus creates a deadlock

<img src="https://howtodoinjava.com/wp-content/uploads/2012/10/deadlock1.jpg" />

A thread is in blocked state when it is waiting for a lock which is currently held by any other thread or is in sleep, waiting for I/O.
<img src="https://static.javatpoint.com/images/thread-life-cycle.png" />

There are multiple ways to detect the states of threads currently in execution.