---
layout: post
title: Simple configure for rsync
category: tech
---
***
###Server

>rsync --daemon --port=3000
>vim /etc/rsyncd.conf
>vim /etc/rsyncd.pwd


###Client

>rsync -az --progress /source/ hero@127.0.0.1::path/ --port=3000 --password-file=rsync.password
>chmod 600 rsync.password
