---
layout: default-en
title: Config file parser
project_slug: config
tags: C, utils
lang: en
---

## About project
<p>Recently I felt necessity in abillity to read config files in programs(files in human-readable format). I didnt want to use "heavy" formats like json or yml and use side heavy libraries for working with them. So I decided to use simple format like that:
<pre style="background: #bebebe;"><code >KEY=VALUE
hellow=world
list = ["ds", "124", "ewe]
</code></pre>
and write my own parsing program.</p>  
So this program appeared because of my own need in it and my wish to work with low level parsing.

## Links
[GitHub Repo](https://github.com/ExtremumDev/config_reader)

## Tech stack
Plain C
## Current status
Developing  
Simple version is ready. There is an abillity to read simple key=value configs(without lists for now). I am planning to upgrade this program perfectly(parsing itself and usability for it's users).
I would like to some people to use and test my program in their projects and give feedback 