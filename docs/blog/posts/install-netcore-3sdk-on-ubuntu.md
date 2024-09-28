---
title: "Install NetCore 3 SDK on Linux Ubuntu 16.04 X64"
date: 2019-10-28T21:58:09+01:00
draft: false
tags: [ ".NetCore", "Linux", "WLS" ]
---

On my desktop at home I am running Windows 10 Pro, but i really like to play around with Linux distributions, because I think it is important to know these OS's as a developer.
Therefore I have installed "Windows Subsystem for Linux" also known as WLS. This is a compatibility layer for running Linux executables (ELF format) on Windows 10.

I always tend to forget how to keep the Linux environment up to date, with the newest version of my different tools, because I am running mostly on Windows.
Therefore here is a little guide on how to keep your .NetCore SDK up to date.

![Headache](../images/oh-no-i-forgot-something.jpg)

# Register Microsoft key and feed
Before installing .Net Core, you'll need to register the Microsoft key, register the product repository, and install required dependencies. This only needs to be done once per machine.

Open a terminal and run the following commands:
```bash
  wget -q https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
  sudo dpkg -i packages-microsoft-prod.deb
```

# Install the .NET SDK
In your terminal, run the following commands:

```bash
  sudo apt-get update
  sudo apt-get install apt-transport-https
  sudo apt-get update
  sudo apt-get install dotnet-sdk-3.0
```

And viola. Now verify that you have the newest version of .Net Core 3 by typing the following in the terminal:

```bash
  dotnet --info
```

Now you are ready to go program with the new awesome .Net Core 3