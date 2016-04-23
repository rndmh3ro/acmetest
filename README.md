# letest
Unit test project for le project https://github.com/Neilpang/le



# Here are the latest status:

| Platform | Status| Last Run Time| Comments|
-----------|-------|--------------|---------|
|windows-cygwin| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/windows-cygwin.svg?1461388681)| Sat, Apr 23, 2016  5:18:01 AM| Passed |
|freebsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/freebsd.svg?1461381345)| Sat Apr 23 03:15:45 UTC 2016| Passed |
|ubuntu:14.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-14.04.svg?1461423972)| Sat Apr 23 15:06:12 UTC 2016| Passed |
|ubuntu:15.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-15.04.svg?1461424362)| Sat Apr 23 15:12:42 UTC 2016| Passed |
|ubuntu:16.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-16.04.svg?1461424990)| Sat Apr 23 15:23:10 UTC 2016| Passed |
|ubuntu:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-latest.svg?1461425357)| Sat Apr 23 15:29:17 UTC 2016| Passed |
|debian:7| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-7.svg?1461425715)| Sat Apr 23 15:35:15 UTC 2016| Passed |
|debian:8| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-8.svg?1461426090)| Sat Apr 23 15:41:30 UTC 2016| Passed |
|debian:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-latest.svg?1461426460)| Sat Apr 23 15:47:40 UTC 2016| Passed |
|centos:5| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-5.svg?1461426770)| Sat Apr 23 15:52:50 UTC 2016| Failed |
|centos:6| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-6.svg?1461427527)| Sat Apr 23 16:05:27 UTC 2016| Failed |
|centos:7| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-7.svg?1461427938)| Sat Apr 23 16:12:18 UTC 2016| Passed |
|centos:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-latest.svg?1461428349)| Sat Apr 23 16:19:09 UTC 2016| Passed |
|fedora:21| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-21.svg?1461428763)| Sat Apr 23 16:26:03 UTC 2016| Passed |
|fedora:22| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-22.svg?1461429158)| Sat Apr 23 16:32:38 UTC 2016| Passed |
|fedora:23| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-23.svg?1461429549)| Sat Apr 23 16:39:09 UTC 2016| Passed |
|fedora:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-latest.svg?1461429933)| Sat Apr 23 16:45:33 UTC 2016| Passed |
|opensuse:13.2| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/opensuse-13.2.svg?1461430291)| Sat Apr 23 16:51:31 UTC 2016| Passed |
|opensuse:42.1| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/opensuse-42.1.svg?1461430647)| Sat Apr 23 16:57:27 UTC 2016| Passed |
|opensuse:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/opensuse-latest.svg?1461431363)| Sat Apr 23 17:09:23 UTC 2016| Passed |
|alpine:3.1| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/alpine-3.1.svg?1461431663)| Sat Apr 23 17:14:23 UTC 2016| Passed |
|alpine:3.2| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/alpine-3.2.svg?1461431961)| Sat Apr 23 17:19:21 UTC 2016| Passed |
|alpine:3.3| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/alpine-3.3.svg?1461432243)| Sat Apr 23 17:24:03 UTC 2016| Passed |
|alpine:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/alpine-latest.svg?1461432526)| Sat Apr 23 17:28:46 UTC 2016| Passed |
|oraclelinux:6| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/oraclelinux-6.svg?1461432969)| Sat Apr 23 17:36:09 UTC 2016| Passed |
|oraclelinux:7| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/oraclelinux-7.svg?1461433362)| Sat Apr 23 17:42:42 UTC 2016| Passed |
(The openssl in CentOS 5 doesn't support ECDSA, so the ECDSA test cases failed. However, RSA certificates are working there.)

# How to run tests

First point at least 2 of your domains to your machine, 
for example: `aa.com` and `www.aa.com`

And make sure 80 port is not used by anyone else.

```
cd letest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./letest.sh
```

# How to run tests in all the platforms through docker.

You must have docker installed, and also point 2 of your domains to your machine.

Then test all the platforms :

```
cd letest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./rundocker.sh  testall
```

The script will download all the supported platforms from the official docker hub, then run the test cases in all the supported platforms.






