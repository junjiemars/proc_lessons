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
PATH=$ORACLE_BASE:$ORACLE_HOME:$PATH
export PATH
```

### 

## References
* [Introduction to Pro*C Embedded SQL](http://infolab.stanford.edu/~ullman/fcdb/oracle/or-proc.html)
* [Pro*C/C++ Programmer’s Guide](http://docs.oracle.com/cd/E11882_01/appdev.112/e10825/toc.htm)
