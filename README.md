This is a folk of [cyg-fast](https://github.com/tmshn/cyg-fast).

apt-cyg
=======

apt-cyg is an advanced version of apt-cyg, command-line installer for [Cygwin](http://cygwin.com/) which cooperates with Cygwin Setup and uses the same repository.

Supporting pre-resolving dependencies and parallel-downloading, apt-cyg works faster than apt-cyg.

The syntax is similar to apt-get. Usage examples:

* "apt-cyg install &lt;package names&gt;" to install packages
* "apt-cyg resume-install" to resume interrupted installing
* "apt-cyg remove &lt;package names&gt;" to remove packages
* "apt-cyg update" to update setup.ini
* "apt-cyg show" to show installed packages
* "apt-cyg find &lt;pattern(s)&gt;" to find packages matching patterns
* "apt-cyg describe &lt;pattern(s)&gt;" to describe packages matching patterns
* "apt-cyg packageof &lt;commands or files&gt;" to locate parent packages
* "apt-cyg pathof &lt;cache|mirror|mirrordir|cache/mirrordir&gt;" to show path"

Requirements
-----------

apt-cyg requires the cygwin default environment and optional packages below.

* aria2

Quick start
-----------

apt-cyg is a simple script. Once you have a copy, make it executable:

    # chmod +x /bin/apt-cyg

Optionally place apt-cyg in a bin/ folder on your path.

Then use apt-cyg, for example:

    # apt-cyg install vim

New features
------------

### Parallel downloading with aria2

Aria2 is an advances file downloading tool that allows you to download files with faster speed.

apt-cyg provides multi-connection downloading using aria2.

You can change the maximum number of connections with the ```--max-connections``` option.

### True multi-architecture support

Let think a case that you want to install the x86 package when you are working under the x86_64 environment.
For example:

    # apt-cyg --charch x86 install chere

As of 2013-10-26, chere package is provided for only the repository for x86.

Remarks:
Of course, you must install both environments of x86_64 and x86, beforehand.

### Pre-resolving dependencies

apt-cyg finds all depending packages before downloading and installing.

### Check dependency on removing

You can remove all packages depending on packages you want to remove.

### Resume installation when downloading fails

Type ```apt-cyg resume-install``` to resume interrupted downloading.

You don't need to be annoy with an unstable internet connection...

### Force re-install packages

You can reinstall a package by using ```apt-cyg --force install <package>```

### Rapid mode

If you are hurrying to install some packages, use ```--rapid``` to avoid wasting time
by updating setup.ini, checking certificates, checking signatures, checking MD5s, etc.

Contributing (original apt-cyg)
-------------------------------

This project has been re-published on GitHub to make contributing easier. Feel free to fork and modify this script.

The [Google Code project](https://code.google.com/p/apt-cyg/) has a list of open issues.

### Forks on the github

Caution:
Please do not merge forks that have incompatible licenses.

Ex.) Merging to the GPL from the MIT is possible. But merging to the MIT from the GPL  is impossible.

#### Official (MIT license)

* [transcodes-open / apt-cyg](https://github.com/transcode-open/apt-cyg/network)

#### Unofficial (GPLv2)

* [cfg / apt-cyg](https://github.com/cfg/apt-cyg/network)
* [ashumkin / apt-cyg](https://github.com/ashumkin/apt-cyg/network)
* [svn2github / apt-cyg](https://github.com/svn2github/apt-cyg/network)
* [nosuchuser / apt-cyg](https://github.com/nosuchuser/apt-cyg/network)
* [kazuhisya / apt-cyg64](https://github.com/kazuhisya/apt-cyg64/network)
* [bnormsoftware / apt-cyg](https://github.com/bnormsoftware/apt-cyg/network)
* [rcmdnk / apt-cyg](https://github.com/rcmdnk/apt-cyg/network)
* [buzain / apt-cyg](https://github.com/buzain/apt-cyg/network)
* [wuyangnju / apt-cyg](https://github.com/wuyangnju/apt-cyg/network)
* [takuya / apt-cyg](https://github.com/takuya/apt-cyg/network)

