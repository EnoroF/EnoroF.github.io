---
layout: post
title: Apache Lucene - Query Parser Syntax 
category: tech
---
***
###Terms
- there are two types of term.
- single term like "hello".
- pharse term like "hello world".
- multiple terms can be combined together with boolean operators to form complex query.

###Fields
- search a field by typing the field name followed by a colon ":".
- title:"hello" AND message:"world"
- title:"hello" AND "world"

###Wildcard Searches
- "?" as single character
- "*" as none or more then one character

###Fuzzy Searches
- use a "~" to use fuzzy search, 
- room~
- room~0.8

###Proximity Searches
- "hello"~10

###Range Searches
- date:[20151101 TO 20151105]
- include 20151101 and 20151105
- title:{hello TO world}
- do not include hello and world

###Boolean Operators
- AND "+" OR NOT "-"


### Escaping Special Characters
- + - && || ! ( ) { } [ ] ^ " ~ * ? : \
- use \ before these characters.