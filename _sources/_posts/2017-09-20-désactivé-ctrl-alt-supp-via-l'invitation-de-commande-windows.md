---
layout: post
title: "Désactivé CTRL+ALT+SUPP via l'invitation de commande Windows"
date: 2017-09-20
categories: windows
tags: [windows, terminal, regedit]
---
**1)** Ouvrir une invitation de commandes en tant qu'administrateur  
  
![](https://2.bp.blogspot.com/-anMG8Y79dA4/VmIW4TsJtcI/AAAAAAAAEXA/I6uWq2nx1cg/s1600/oem_1.png)  
  
**2)** Changer la valeur de la clef de registre **disablecad** pour **00000001**

reg add "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System" /V disablecad /T REG\_DWORD /D "00000001" /f

  
**3\*)** Pour réactiver CTRL + ALT + SUPP il suffit de remettre la valeur à **00000000**

reg add "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System" /V disablecad /T REG\_DWORD /D "00000000" /f

  

**[top-password.com](https://www.top-password.com/blog/2-options-to-disable-press-ctrlaltdel-to-log-on-in-windows/)**