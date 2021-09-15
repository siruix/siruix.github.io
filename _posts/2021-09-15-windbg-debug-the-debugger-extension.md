---
layout: post
title:  "Windbgx: How to debug a debugger extension"
date:   2018-03-15 17:22:01 -0600
categories: Windows Windbg
---
Have you ever use a windbg debugger extension and that debugger extension has bugs in it? How to debug a debugger extension? This post shows the steps to use windbgx to another windbgx process. 

### Windbgx A attaches to a target process
The target process to be attached depends on the debugger extension. Let's say the debugger extension is to parse the memory dump of vmwp.exe process. Windbg A should attach to vmwp.exe. Then load the debugger extension into windbgx A. 

### Windbgx B attaches to Enghost.exe process
The debugger extension in the previous step is loaded into Enghost.exe process. Windbgx B should attach to Enghost.exe. Once attached, you should be able to search the debugger extension symbols. 

![Windbgx_B](/assets/Windbgx-B.PNG)
