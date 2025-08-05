---
layout: post
title: Process synchronization - An easy explanation
date: 2025-07-10
categories: os
author: insane
permalink: /posts/process-synchronization-an-easy-explanation
tags:
  - os
  - processes
  - synchronization
---

![Thumbnail for the post](/assets/process-synchronization-an-easy-explanation/thumbnail.webp)

**Process Synchronization** is simply about running multiple processes that are accessing the same common resource (or resources) in a specific, controlled order so that everything goes smoothly and there’s no conflict.

Here, multiple processes (or even threads) could be sharing resources like a file, a database, or some part of the memory — and synchronization ensures that they don’t mess things up for each other.

A simple example:  
Imagine we have a database and two programs – Program A and Program B.

- Program A is responsible for adding/ updating (writing) a record to the database.
- Program B is responsible for reading a record from the database.

![Diagram illustrating a database with 5 rows and two process A and B. Process A wants to update record 5 while at the same time process B wants to read record 5. This makes the database sad as these are two conflicting types of operations being performed at the same time](/assets/process-synchronization-an-easy-explanation/diagram.webp)

Now, there are 5 records in the database. Program B wants to read record 5, while Program A wants to edit and update record 5. If both programs attempt to access the record simultaneously, it could lead to problems, such as Program B reading a half-updated record.  
  
To avoid this, **synchronization** is essential. The solution here is to lock the resource while either program is using it. If Program B decides to read record 5, the database should be locked from Program A’s access. This ensures that Program B reads the complete, unaltered data. (However program B here would be reading old data which is later updated)  
  
Similarly, when Program A is updating the record, the database should be locked for Program B’s access. Once Program A has finished updating this lock is released.  
  
**Note:** Multiple programs that only want to read from the same database can do so simultaneously without locking each other out. This is because reading data doesn’t change anything, so one program’s reading doesn’t affect another’s.  
  
Well that was all.
🦖
