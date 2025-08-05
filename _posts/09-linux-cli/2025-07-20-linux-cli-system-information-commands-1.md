---
layout: post
title: Linux CLI - System information commands
date: 2025-07-20
categories: linux cli
author: insane
permalink: /posts/linux-cli-system-information-commands-1/
tags:
  - linux
  - cli
  - system
  - commands
---

![Thumbnail for the post](/assets/linux-cli/linux-cli-system-information-commands-1/thumbnail.webp)

<br>

> _Inspired from hack the box academy linux tutorials_

<br>

These are some commands which can help you get information about your system. Knowing them might come handy in times of troubleshooting.  
  
I have broken down the commands into chunks of 5 at a time, so I can take time and provide you with proper examples.

<br>

1. **hostname** – Prints the name that you named your linux system while installing it.
   
   ![Output of hostname command](/assets/linux-cli/linux-cli-system-information-commands-1/hostname-cmd.webp)
   
   The hostname (or simply name) of this system is **ubuntuServer**

---

2. **whoami** – Prints the name of the user currently using the terminal.  
  
   **Note:** You might login into the system via different user and then switch to a different user. It will show the most recent user you switched to.
   
   ![Output of whoami command](/assets/linux-cli/linux-cli-system-information-commands-1/whoami-cmd.webp)
   
   Currently a user called **insane** is using the terminal.

---

3. **id** – This command simply commands expands on the whoami commands and provides more information like groups the user is into, their respective group ids and userid of the user.
   
   ![Output of id command](/assets/linux-cli/linux-cli-system-information-commands-1/id-cmd.webp)
   
   User **insane’s** userid is **1000**. His primary group is also called **insane** with group id being **1000** (same as userid). Apart from that he is in **groups** – **user** (group id: **100**), **developers** (group id: **1001**), **docker** (group id: **1002**).

---

4. **uname** – Prints basic information about the system.

   ![Output of uname command](/assets/linux-cli/linux-cli-system-information-commands-1/uname-cmd.webp)
   
   It simply returns name of the **kernel** which is **linux**.  
   **Uname** command combined with some flags becomes very powerful and handy, but its a topic for some other time.

---

5. **who** – Prints who is currently logged in (like whoami) with some little bit of extra information. It also shows from which virtual terminal user logged in, when did he logged in and ipv4 address of the system.
   
   ![Output of who command](/assets/linux-cli/linux-cli-system-information-commands-1/who-cmd.webp)
   
   I logged into this system/ server via **root** user (later I changed to a user called **insane** to run all the commands including this one). I logged in via **virtual terminal 0**. It also shows **date and time** of login and **ipv4** **address** of this system .  
  
   **Virtual terminal** can be thought of as **independent sessions** or **workspaces** for simplicity but it has some quirks. Its not your typical workspaces. In any linux system their are like 6-7 virtual terminals which can be switched via ctrl+alt+f2/f3/etc. I will explain this particular in detail in future probably using a video format in youtube.
   
---

That’s it for this post.  
Hope you like it :] .  
🦖