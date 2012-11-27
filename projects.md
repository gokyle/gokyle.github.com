---
layout: page
title: "Go Projects"
description: "Curated Tour of Kyle Isom's Go projects."
---
{% include JB/setup %}

![Go gophers from the Go homepage](/images/gopher/project.png)

### Web Services
* [urlshorten-ng](https//gokyle.github.com/urlshorten_ng) is a simple URL
shortening service; an example of the service is currently running on
[nodality.io](https://nodality.io).

* [webshell](http://gokyle.github.com/webshell) is a simple framework
for developing web services in Go.

* [golobsters](http://gokyle.github.com/golobsters/) is an application
running on [Heroku](http://www.heroku.com) that posts new stories from
[lobste.rs](https://lobste.rs) to [Twitter](https://www.twitter.com/lobsternews).
It is based on the [rsstotwitter](https://gokyle.github.com/rsstotwitter)
package.

### Standalone Commandline Programs

* [srvwd](http://gokyle.github.com/srvwd) is a simple file server that supports
chrooting for security, dropping privileges, and TLS. It is a rewrite of a
[version I wrote in C](http://tyrfingr.is/projects/srvwd/); for my primary
use case, see
[minimal web development with rawk and srvwd](http://tyrfingr.is/essays/essay_minimal_webdev.html).

* [gotoma](https://github.com/gokyle/gotoma) is a command line tool
for doing pomodoros.

* [say](https://github.com/gokyle/say) is a command line interface to
festival, inspired by the OS X command `say`.

* [gack](https://github.com/gokyle/gack) is an [ack](http://betterthangrep.com/)
clone written in Go. It currently supports basic querying and file listings, 
but has a long ways to go to beat ack's performance.

### Conviennce Packages

* [goconfig](http:/gokyle.github.com/goconfig) is a package for parsing simple
configuration files.

* [goirc](https://gokyle.github.com/goirc) is a library for connecting to an
IRC server.

* [gomon](http://gokyle.github.com/gomon/) provides basic runtime monitoring 
and program restarts for Go programs. It was adapted from a Python module I
wrote for keeping a Bitcoin trading system online.

* [gopush](http://gokyle.github.com/gopush/) provides [Pushover](https://www.pusover.net)
notifications from Go.
