---
layout: single
title:  "How to determine your current logon server/domain controller on Windows 7/8/8.1"
date:   2012-01-19 08:00:00 +0200
categories: tech
---
If you ever need to find your current logon server on Windows 7 (don't know by heart if it also works on XP), you can just run the following command on your command line:

echo %logonserver:*\\=%

UPDATE 2015-Jan-12: also works on Windows 8/8.1

%logonserver% is a local variable with a value that looks like \\domaincontroller. With :*\\= you can strip the leading backslashes and get only the hostname as a result. I have no clue about the value of the variable if you start your machine without a network connection or a connection to a domain controller. It's just a quick&dirty solution and in my case it does the job.