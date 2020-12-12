---
title: "DOWNLOAD GITHUB PROFILE USING COMMAND PROMPT"
date: 2020-12-08T08:06:25+06:00
hero: /posts/introduction/hero.svg
description: How can we download github profile using windows command prompt?
menu:
  sidebar:
    name: Introduction
    identifier: introduction
    weight: 10
---

 - Guys,Hope you are well and think new stuff. Today i'll show you how can we download github users profile data using windows command prompt.
- Well i want to clear here, you can  only download directory which is public not private.
- So, i know you and not intrested in reading much and here for show direct action in short words. Firstly let's see actual **bash** script and then we'll talk about working and more.
```bash
CNTX={users}; NAME={pritam-raj}; PAGE=1
curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" |
  grep -e 'git_url*' |
  cut -d \" -f 4 |
  xargs -L1 git clone
```
- AS i think you try to understand what's going here.Well sometimes we only want our work done without dig dipper.**So** you need to  follow some steps.
  
     - Create folder on Desktop with whatever name you want. **ctrl+shift+N**   HotKey for create folder using command prompt.

     - open Command prompt there using **shift** with **right click** and *click* on *option* *Open Powershell Windows here*.
     - Change ```Name={paste github profile name}```
       -  Ex:- if url is **https://www.github.com/pritam-raj**.
       -  Then only copy name after "/" that is **pritam-raj** and paste insite the **{}**.
  -  Then paste this code and press **Enter**.That's it👍
  -  Wait until its done.
- Always remember github page max download limit at once is only **100** pages.if more Then **Increase** only ```per_page``` value on code.
  
Done for today.we'll meet in next blog with another cool stuff.**Please** comment if you  facing any kind of issue. [Thanks](https://pritam-raj.github.io)

