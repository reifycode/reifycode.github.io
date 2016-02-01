---
layout: post
published: true
exacttime: "12:05:00"
title: "apt-get update fails"
category: "ubuntu"
headimg_url: "/images/ubuntu/ubuntu.jpg"
author: thepulkitagarwal
---

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">[1/2] apt-get update was showing errors, and on trying to fix it, I broke a lot of other stuff, and ended up reinstalling ubuntu. Twice.</p>&mdash; Pulkit Agarwal (@thepulkit13) <a href="https://twitter.com/thepulkit13/status/693835918168322048">January 31, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">[2/2] Finally found out that nothing was wrong with me, but there is a bug in apt-get. And there&#39;s a way around it: <a href="https://t.co/uxDuomZFPh">https://t.co/uxDuomZFPh</a></p>&mdash; Pulkit Agarwal (@thepulkit13) <a href="https://twitter.com/thepulkit13/status/693836337368051712">January 31, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

`E:Unable to Locate Package `

`W: Failed to fetch bzip2:/var/lib/apt/lists/partial/in.archive.ubuntu.com_ubuntu_dists_trusty-backports_main_i18n_Translation-en  Hash Sum mismatch`

`E: Some index files failed to download. They have been ignored, or old ones used instead.`

`Failed to fetch http://archive.ubuntu.com/ubuntu/dists/trusty/Release  Unable to find expected entry 'universe/binary-amd64/Packages' in Release file (Wrong sources.list entry or malformed file)`

These errors, and a lot of others cause a lot of problems for a lot of people. For example, mysql, node and a lot of other packages won't be installed if you get any problems due to this.

And these errors can be traced to this [bug](https://bugs.launchpad.net/ubuntu/+source/ubuntu-release-upgrader/+bug/1373598). So, unless this is fixed, this will remain a problem. There are a lot of ways to go around the problem in the [bugs page](https://bugs.launchpad.net/ubuntu/+source/ubuntu-release-upgrader/+bug/1373598) that I mentioned earlier. Try one of those.

For me, changing the server to a different server in [Software & Updates](https://help.ubuntu.com/community/Repositories/Ubuntu#Ubuntu_Software_Tab) fixed the problem.
