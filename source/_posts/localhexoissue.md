---
title: Local hexo not found error
intro: Local hexo not found error is an annoying error while developing blogs using Hexo.io
date: 2017-01-14 00:00:00
comments: true
author: Vasubabu
---

[Hexo.io](www.hexo.io) is a good blogging framework built on node.js. But some people face issues while installing in Ubuntu or Mac. Local `hexo` not found is one of those.

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

Uninstall `Node.js` and `npm` and install node.js using Node version manager `NVM`.

I would recommend installing node using Node Version Manager(NVM). That saved a lot of head ache for me. Because you can install nodejs and npm without sudo using nvm.


``` bash
$ sudo apt-get remove nodejs
$ sudo apt-get remove npm
```

``` bash
$ sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node* /usr/local/lib/dtrace/node.d ~/.npm ~/.node-gyp /opt/local/bin/node opt/local/include/node /opt/local/lib/node_modules
$ sudo rm -rf /usr/local/lib/node*
$ sudo rm -rf /usr/local/include/node*
$ sudo rm -rf /usr/local/bin/node*
```

Check for any .npm or .node folder in your home folder and delete those.

If you type

``` bash
$ which node #output should be empty
```

## Install `NVM`

To install `nvm` i suggest you to refer this `Digitalocean post` [Install NVM](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-an-ubuntu-14-04-server#how-to-install-using-nvm)

once `nvm` is setup properly, run again these commands

``` bash
$ cd blog_folder
$ npm install
$ npm install -g hexo hexo-cli hexo-server
$ hexo generate
$ hexo server
```

Happy Blogging :) 
