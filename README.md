# proc-tutorial
Oracle Pro*C Programming Tutorial

## Requirements
* Go to [Oracle Instant Client](http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html) 
to download *__Basic__ and __Precompiler__ Instant Client Packages* and take care 32-bit/64-bit that your OS(Mac, Linux or Windows) used.
* C/C++ building environment.

## Setup Pro*C Programming Environment

### Install *__Basic__ and __Precompiler__ Instant Client Packages*

### Setup Environment Variables

**On Linux/Mac**

In **~/.bashrc** file to setup $ORACLE_BASE, $ORACLE_HOME, Pro*C Include Path and Library Loading Path.

```shell
ORACLE_BASE=$HOME/<instant-client-parent-dir>
ORACLE_HOME=$ORACLE_BASE/<instant-client-dir>
export ORACLE_HOME
if [[ -z ${LD_LIBRARY_PATH} ]]; then
  LD_LIBRARY_PATH=$ORACLE_HOME
else
  LD_LIBRARY_PATH=$ORACLE_HOME:$LD_LIBRARY_PATH
fi
export LD_LIBRARY_PATH
PATH=$ORACLE_BASE:$ORACLE_HOME:$ORACLE_HOME/sdk:$PATH
export PATH
```

### Setup Pro*C Configuration File

The default Pro*C configuration at $ORACLE_HOME/precomp/admin/__pcsfg.cfg__, just like:

```shell
sys_include=($ORACLE_HOME/sdk/include,X,Y,Z...)
ltype=short
```

We need to change __sys_include__ base on your C/C++ building environment, so run 

```shell
cc -c -E x.c | grep include
```

filte out the unique __include__ paths from *stdout* then replace **X**, **Y**, **Z** with it in __pcsfg.cfg__ file.

## Pro*C Programming

* A Simple Pro*C Source File: simple.pc
* Makefile



## Build

***On Linux/Mac***

```shell
make -f p.mk
```

## Run

***On Linux/Mac***

```shell
ORA_CONN="<username>/<password>@<remote-address>:<port>/<sid>" ./p
```



## References
* [Introduction to Pro*C Embedded SQL](http://infolab.stanford.edu/~ullman/fcdb/oracle/or-proc.html)
* [Pro*C/C++ Programmer’s Guide](http://docs.oracle.com/cd/E11882_01/appdev.112/e10825/toc.htm)
