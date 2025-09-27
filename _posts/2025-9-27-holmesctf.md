---
title: "holmesctf"
date: 2025-09-27
---

This is the first time I participate in a all blue CTF, I am here to write some simple writeups so that I don't forget what I learned.


For browsing evtx files, I found that many people were using the setup EvtxeCmd and TimelineExplorer. Which can be found [here](https://ericzimmerman.github.io/#!index.md).

By executing the following command, convert the evtx file under the logs folder to a csv file:
```ps1
.\EvtxECmd.exe -d "D:\ctf\holmes-2025-9-22\The_Enduring_Echo\The_Enduring_Echo\C\Windows\System32\winevt\logs" --csv . --csvf evtx.csv
```
and then use TimelineExplorer to open the csv file.

To further analyse the events, find the likely event ID. This can be found [here](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/).

Creating a task under `C:/Windows/System32/Tasks` is a common way for persistence.

The registry file is under `C:/Windows/System32/config` and is useful for forensics.

The tool impacket is very useful for various tasks. It can be found [here](https://github.com/fortra/impacket).

