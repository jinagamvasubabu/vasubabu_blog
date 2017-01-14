---
title: Local hexo not found
intro: Local hexo not found error is an annoying error while developing blogs using Hexo.io
date: 2017-01-14 00:00:00
comments: true
author: Vasubabu
---

[Hexo.io](www.hexo.io) is a good blogging platform built on node.js. But some people face issues while installing in Ubuntu or Mac. Local `hexo` not found is one of those.

## Hexo.io

### install hexo with sudo

Install hexo with sudo solves the issue.

``` bash
$ sudo npm install -g hexo
```

### install hexo-server with sudo 

Install hexo-server with sudo to run hexo-server on a default port.

``` bash
$ sudo npm install -g hexo-server
```

### Not Working ??

Delete the node_modules completely in your project and install again and repeat the above two steps again.

``` bash
$ cd blog
$ rm -rf node_modules
$ npm install
```

Please comment below if it still doesn't work
