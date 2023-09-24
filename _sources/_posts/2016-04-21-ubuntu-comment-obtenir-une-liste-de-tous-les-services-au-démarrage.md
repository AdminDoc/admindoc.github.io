---
layout: post
title: "Ubuntu - Comment obtenir une liste de tous les services au démarrage "
date: 2016-04-21
categories: linux
tags: [ubuntu]
---
`initctl list`  
  
  
`+` = En cours d’exécution, `-` = Arrêté. `?` = géré par upstart  
  
  
Commande utile.  
  
initctl list | egrep -v " stop/waiting|^tty" ; service --status-all 2>&1 | egrep -v "\\\[ (\\?|\\-) \\\]"