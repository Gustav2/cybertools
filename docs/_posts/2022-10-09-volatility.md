---
layout: post
title:  "Volatility - Cheatsheet"
date:   2022-10-09 00:00:00 +0200
categories: volatility cheatsheet
permalink: /volatility/
---
### General commands
- `vol2`: Using volatility2 
- `vol3`: Using volatility3
- `-f [image]`: Flag to specify memory image

## Identify OS and architecture
#### Volatility2
{% highlight shell %}
vol2 -f [image] imageinfo
{% endhighlight %}

#### Volatility3
There is no way to make volatility3 find the correct os with just one command. Volatility3 has a command for each os. Windows memdumps tend to be larger than linux dumps.

Windows:
{% highlight shell %}
vol3 -f [image] windows.info.Info
{% endhighlight %}
Linux:
{% highlight shell %}
vol3 -f [image] banners.Banners
{% endhighlight %}
