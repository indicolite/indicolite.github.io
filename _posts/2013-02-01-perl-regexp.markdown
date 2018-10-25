---
layout: post
title: "perl-regexp"
date: 2013-02-01 09:13:17 +0800
comments: true
categories:
---
```
#!/usr/bin/perl
#
use strict;
use warnings;

open(TESTLOG, "./test_0121.txt") || die "$!";
while (<TESTLOG>) {
  my $str=$_;
  while ($str =~ m#(/p/tts[0-9]/[0-9]{6}/[0-9]{1,3}/\w+?\.bmp)#g) {
      print "$1\n";
  }
  #print ".........................$str\n";
}
```