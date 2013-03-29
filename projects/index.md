---
layout: page
title: "Go Projects"
description: "Curated Tour of Kyle Isom's Go projects."
---
{% include JB/setup %}

### Libraries
* [coinbase_api](https://github.com/gokyle/coinbase_api) is a Golang interface
to the [Coinbase](https://coinbase.com) API. It is about 50% complete, but
supports retrieving exchange rates, checking transaction prices, and
buying / selling bitcoins.

* [fswatch](https://github.com/gokyle/fswatch) is a polling UNIX file system watcher.
An operating-system-specific event system is being worked on (i.e. FSEvents for OS X).

* [pbkdf2](http://github.com/gokyle/pbkdf2) is a convenience wrapper
around [go.crypto/pbkdf2](http://go.pkgdoc.org/code.google.com/p/go.crypto/pbkdf2).
It provides simpler `HashPassword` and `MatchPassword` functions, while
using sane (and configurable) HMAC-SHA1 defaults. The output hash
is suitable for use as an AES-256 key.

* [filecache](http://gokyle.github.com/filecache) is a basic file cache
written in pure Go with no external dependencies.

### Web Services
* [gowik](https://github.com/gokyle/gowik) is a simple, single-user wiki
I wrote to replace [gitit](http://gitit.net). It's a bit rough around the
edges, but I currently use it for a personal wiki-like system.

* [urlshorten-ng](http://gokyle.github.com/urlshorten_ng) is a simple URL
shortening service; an example of the service is currently running on
[nodality.io](https://nodality.io).

* [webshell](http://gokyle.github.com/webshell) is a simple framework
for developing web services in Go.

* [golobsters](http://gokyle.github.com/golobsters/) is an application
running on [Heroku](http://www.heroku.com) that posts new stories from
[lobste.rs](https://lobste.rs) to [Twitter](https://www.twitter.com/lobsternews).
It is based on the [rsstotwitter](http://gokyle.github.com/rsstotwitter)
package.

### Standalone Commandline Programs

* [golst](http://gokyle.github.com/golst) is a Go literate programming tool
that generates readable listings from Go source code with no need for any
different syntax than used by GoDoc.

* [cachesrv](http://gokyle.github.com/cachesrv) is the caching version of
[srvwd](http://github.com/srvwd).

* [srvwd](http://gokyle.github.com/srvwd) is a simple file server that supports
chrooting for security, dropping privileges, and TLS. It is a rewrite of a
[version I wrote in C](http://tyrfingr.is/projects/srvwd/); for my primary
use case, see
[minimal web development with rawk and srvwd](http://tyrfingr.is/essays/essay_minimal_webdev.html).

* [gotoma](http://gokyle.github.com/gotoma) is a command line tool
for doing pomodoros.

* [say](https://github.com/gokyle/say) is a command line interface to
festival, inspired by the OS X command `say`.

* [gack](https://github.com/gokyle/gack) is an [ack](http://betterthangrep.com/)
clone written in Go. It currently supports basic querying and file listings, 
but has a long ways to go to beat ack's performance.

### Convienence Packages

* [goconfig](http://gokyle.github.com/goconfig) is a package for parsing simple
configuration files.

* [goirc](http://gokyle.github.com/goirc) is a library for connecting to an
IRC server.

* [gomon](http://gokyle.github.com/gomon/) provides basic runtime monitoring 
and program restarts for Go programs. It was adapted from a Python module I
wrote for keeping a Bitcoin trading system online.

* [gopush](http://gokyle.github.com/gopush/) provides [Pushover](https://www.pusover.net)
notifications from Go.
