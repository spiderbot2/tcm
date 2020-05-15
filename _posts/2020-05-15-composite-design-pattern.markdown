---
layout: post
title:  "Composite Design Pattern!"
categories: [ designpatterns ]
tags: [designpatterns, featured, sticky]
image: https://www.programcreek.com/wp-content/uploads/2013/02/composite-design-pattern.png
excerpt: "Learning about composite design pattern"
---


# Usage

When we need to create a structure and the structure combines with multiple objects which need to be treated the same way, then we can use composite design pattern. As it shows it is a composition of multiple objects. All the objects which combine together are called leafs. The object which is made by combining leafs is called composite. The behaviour exerted by leaf objects and composite objects is the same so they can inherit same behaviour. This can be done by inheriting same abstract class of same interface. This abstract class or interface is called the Base Component.

## So there are 3 elements in total

#### Base
<script src="https://gist.github.com/spiderbot/cd0e200215554afa6b1da74106fb6441.js"></script>

#### Leaf
<script src="https://gist.github.com/spiderbot/e620d3b61ec64649295ffe21ddbd63b0.js"></script>

#### Composite
<script src="https://gist.github.com/spiderbot/3a448daf87be382474dfe57f65de2eac.js"></script>
