---
layout: post
title: "Micro logs #01: Dry run with pacman package manager"
date: 2025-06-13
categories: micrologs linux
author: insane
permalink: /posts/micro-logs-1-dry-run-with-pacman-package-manager
tags: arch linux micrologs
---

![](/assets/micrologs/micrologs-01-dry-run-with-pacman-package-manager/thumbnail-02.webp)

Dry run with pacman package manager

**`Source:`** [https://wiki.archlinux.org/title/Pacman](https://wiki.archlinux.org/title/Pacman)  
**`pacman:`** Package manager for Arch Linux

**``-p``** flag can be used with pacman to **dry run** commands — that is, see what your command is going to do **before** it actually does anything.

Might not work with certain flag combinations like **``-n``**, and it will simply throw an error. 

Flags used in the command -
- **`R`**: **`--remove`** - removes the specified package.
- **`s`**: **`--recursive`** - removes the package and its dependencies that are no longer required by any other installed package.
- **`n`**: **`--nosave`** - removes the package's configuration files as well.

---

**Optional explanation with simple examples** -

**``pacman -Rns`` :** To remove a package and its dependencies which are not required by any other installed package. 

<br>

1. Normal Behavior -
  
   ![pacman -Rs command usage](pacman-rns-command.webp)

<br>

2. **-p** flag works well and shows a list of the final packages which will be removed. It only shows what **`Pacman -Rs`** is going to do instead of asking for deletion confirmation to proceed further. -

   ![pacman -p command usage along with -Rs flags, and everything works well](pacman-rs-p-command.webp)

<br>

3. **``-p``** doesn’t work when used with **``-n``** flag -  
  
   ![pacman -p command usage along with -n flag which returns an error](pacman-rns-p-command.webp)

---

That's it!

Hope you like it.

🦖