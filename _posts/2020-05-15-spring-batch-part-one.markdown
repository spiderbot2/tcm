---
layout: post
title:  "Spring Batch - Part 1 (Introduction)"
categories: [ spring ]
tags: [spring, featured]
image: https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRjZAUi3lecrYEyvAlKiYRlIUpHw2wFhBR5W3oH2l18PnZwmAgmLw&s
excerpt: "In this post we will learn the basics about Sprint Batch."
---

Spring Batch is used to develop batch processing tasks which are used in enterprise applications. Batch processing is a processing mode which involve a series of jobs and do not require user interaction. These jobs process bulk of data and run for long durations. In addition to bulk processing, this framework provides functions for :

*   Including logging and tracing
*   Transaction management
*   Job processing statistics
*   Job restart
*   Skip and Resource management
*   Automatic retry after failure
*   Concurrent jobs execution

Dependencies to enable Spring Batch :

Architecture Of Spring Batch :

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3YZIK4K70m4KMu2Kg0UdFiZFNLnWr6R3aHkchj93mIHPSv6gcOw&s)

The architecture contains three main components namely, Application, Batch Core, and Batch Infrastructure.

1.  Application : This component contains all the jobs and the code we write using the Spring Batch framework.
2.  Batch Core : This component contains all the API classes that are needed to control and launch a Batch Job.
3.  Batch Infrastructure : This component contains the readers, writers, and services used by both application and Batch core components.

  

Components Of Spring Batch Application

![](https://i1.wp.com/learningsolo.com/wp-content/uploads/2018/04/partitioning-overview.png?resize=800%2C445)

1.  Job : A job is a batch process which needs to be executed. It will run and complete without interruption.
2.  Step : A step is an independent part of a job which contains the necessary information to define and execute the job (its part). A job consists of one or more steps.
3.  Readers, Writers, and Processors : An item reader reads data into a Spring Batch application from a particular source, whereas an item writer writes data from the Spring Batch application to a particular destination. An Item processor is a class which contains the processing code which processes the data read into the spring batch. If the application reads "n" records, then the code in the processor will be executed on each record.Spring batch by default provides many Readers and Writers and we can use them by injecting them in our application as per use.
4.  JobRepository : A Job repository in Spring Batch provides Create, Retrieve, Update, and Delete (CRUD) operations for the JobLauncher, Job, and Step implementations. In case we dont want to persist the implementation we can use in-memory repository also.
5.  JobLauncher : JobLauncher is an interface which launces the Spring Batch job with the given set of parameters. SimpleJoblauncher is the class which implements the JobLauncher interface.
6.  JobInstance : A JobIinstance represents the logical run of a job; it is created when we run a job. Each job instance is differentiated by the name of the job and the parameters passed to it while running.
7.  JobExecution and StepExecution : JobExecution and StepExecution are the representation of the execution of a job/step. They contain the run information of the job/step such as start time (of job/step), end time (of job/step).
