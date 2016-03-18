---
layout: post
published: false
exacttime: "10:57:00"
title: "GNU GCC on a Mac"
category:
- "C"
- "Compilers"
author: shreyashpatodia
---

Greetings everyone !! 

So there is something really interesting about the GCC compiler that comes bundled with XCode, it's not GCC at all. It is a variation and is called clang. You can test this out by running the command: 

`gcc -v`

So, recently I had to compile a file containing nested functions and it so turns out that since nested functions are not ISO C, clang very conveniently throws an error as soon as you encounter them. Now, since I can't modify the source file I am working with I had to go ahead and download GNU GCC on my computer, which as it turns out isn't as simple as building a program in C.

Start off by downloading the following things:


- [GNU GCC](http://mac.softpedia.com/get/Development/Compilers/GCC.shtml)

- [GMP Library](https://gmplib.org/)

- [GNU MPFR](http://www.mpfr.org/mpfr-current/#download)

- [MPC](http://www.multiprecision.org/index.php?prog=mpc&page=download)

Once you have downloaded everything, maybe in the downloads folder navigate there using the cd command and then run: 

`cd gmp-*`

Make a directory called build and navigate to it: 

`mkdir build`
`cd build`

Next run:

`../configure --prefix=/usr/local/gcc-5.2.0 --enable-cxx`

You should get something that looks like this: 

`Version:           GNU MP 6.1.0
Host type:         haswell-apple-darwin15.3.0
ABI:               64
Install prefix:    /usr/local/gcc-5.2.0
Compiler:          gcc
Static libraries:  yes
Shared libraries:  yes`


We can now actually compile the makefile: 

`make -j 4`

`make install`

It may ask you to run `make check` and if it does then I would also suggest you do the same. We will do to do the whole procedure for mpfr and mpc as well:

Navigate to the mpfr directory:

`cd ../../mpfr-*`
`mkdir build`
`cd build`
`../configure --prefix=/usr/local/gcc-5.2.0 --with-gmp=/usr/local/gcc-5.2.0`
`make -j 4`
`make install`

For MPC:

`mkdir build`
`cd build`
`../configure --prefix=/usr/local/gcc-5.2.0 --with-gmp=/usr/local/cc-5.2.0 --with-mpfr=/usr/local/gcc-5.2.0`
`make -j 4`
`make install`



We can build gcc now: 

`cd ../../gcc-*`
`mkdir build`
`cd build`
`../configure --prefix=/usr/local/gcc-5.2.0 --enable-checking=release --with-gmp=/usr/local/gcc-5.2.0 --with-mpfr=/usr/local/gcc-5.2.0 --with-mpc=/usr/local/gcc-5.2.0 --enable-languages=c,c++,fortran`





