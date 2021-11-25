---
layout: single
title:  "The trust relationship between this workstation and the primary domain failed"
date:   2012-02-03 08:00:00 +0200
categories: tech
---
Temporarily:
{% highlight bash %}
ifconfig eth0 down
ifconfig eth0 hw ether 00-11-22-33-44-AA
ifconfig eth0 up
{% endhighlight %}

Permanently:
{% highlight bash %}
vi /etc/network/interfaces
{% endhighlight %}

{% highlight bash %}
iface eth0 inet dhcp
  hwaddress ether 00-11-22-33-44-AA
{% endhighlight %}
Got an error?

`SIOCSIFHWADDR: Operation not permitted`

Make sure you're root.