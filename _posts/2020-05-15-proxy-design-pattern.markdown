---
layout: post
title:  "Proxy Design Pattern!"
categories: [ designpatterns ]
tags: [designpatterns, featured]
image: https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQWZj9ztQZGTruRgeJGtwb8AI6S0fM_KPcFvWK8-cL7vWtipvR21w&s
---


# Usage

When we need to control access to some object, mainly due to security reasons, then this design pattern comes in use. There are 3 design participants in this design pattern.

*   Subject : The Interface which provides the core functionality
*   Real Subject : The object which implements the functionality exposed by the Subject
*   Proxy : The object which controls the access to the Real Subject.

Let’s say we have a class that can run some command on the system. Now if we are using it, its fine but if we want to give this program to a client application, it can have severe issues because client program can issue command to delete some system files or change some settings that you don’t want. Here a proxy class can be created to provide controlled access of the program.

### Code Block Example
<script src="https://gist.github.com/spiderbot/cce445c1fedf058640bd7411bc19687d.js"></script> 

Java RMI package uses proxy pattern. That’s all for proxy design pattern in java.
