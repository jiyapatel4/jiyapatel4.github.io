---
title: "OSTEP Musings: Ch.2 Introduction to Operating Systems"
date: 2026-04-09
---
The purpose of the OS is distilled and pure: to make the system easy to use. I was beyond delighted to learn that before the modern OS was conceived, there was a human operator who ran programs one at a time and maintained the "integrity" of the queue order. I can almost imagine it, Jeff, a disgruntled employee, standing in front of the cumbersome mainframe with a minute to go before lunch, and he decides running your job can wait. Jeff clearly has his priorities straight. 

The history of the OS is vast, but a few points stuck out to me. 

† The main idea of this chapter was to introduce the concepts of virtualizing resources such as the CPU, memory, and disk, the strange behaviour of concurrency and atomic instructions, and the persistence of data. All in the hopes of making the system easy to use, while balancing real-world trade-offs, constraints, and the siren’s song of perfection.

† The code running the OS should be treated differently from standard program code; that’s because the OS interfaces with core I/O hardware and parts of the system that could be misused by threat actors or unwittingly corrupted by an intern, like me. System calls were introduced to toggle between user mode and kernel mode, restricting physical memory access and special I/O operations to the OS.

† Instead of running jobs one at a time, multiprogramming creates the illusion of multiple programs running simultaneously. When a process is blocked on a heavy I/O operation, the CPU can be yielded to another process, improving CPU utilization. This sheds light on the importance of memory protection and ensuring different programs can’t tamper with each other’s memory.

† Microsoft’s DOS (Disk Operating System) lacked memory protection, meaning errant or malicious programs could create a palimpsest of memory. Moreover, the neophyte Mac OS line used cooperative scheduling, which meant any rogue thread could go on a rampage and refuse to yield control of the CPU. 

† I was surprised to learn that the UNIX OS was freely distributed, a pioneering move for open-source software! While the ensuing legal battles and the race to own, conquer, and control the new technology were grim, it wasn’t shocking. Eventually, Linux stepped onto the stage and propelled the open-source movement. When I think of big tech companies like Google and Facebook, I never considered that the operating systems they use are based on Linux. It feels odd that their entire monopoly essentially blossomed from transparent source code, while their products obfuscate. I suppose open-source and big tech share a symbiotic relationship that I can’t even begin to decipher, given what little I know.  