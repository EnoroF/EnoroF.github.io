---
layout: post
title: Two configure for Logstash
category: tech
---
***
###Shipper

>input
>{
>    file
>	{
>        path => "C:\Users\EnoroF\Desktop\logstash-2.0.0\bin\1.txt"
>		sincedb_path => "C:\Users\EnoroF\Desktop\logstash-2.0.0\bin\2.txt"
>    }
>}
>
>output
>{
>    stdout
>    {
>    }
>    
>    redis
>    {
>        host => "192.168.0.89"
>        port => 6379
>        data_type => "list"
>        key => "logstash"
>    }
>}


###Indexer
>input
>{
>	redis
>	{
>		host => "192.168.0.89"
>		port => "6379"
>		key => "logstash"
>		data_type => "list"
>		codec  => "json"
>		type => "logstash-arthas-access"
>		tags => ["arthas"]
>	}
>}
>
>output
> {
>	elasticsearch
>	{
>		hosts => "127.0.0.1"
>		index => "logstash-arthas-access-%{+YYYY.MM.dd}"
>	}
>}
