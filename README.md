
# MiniSAT-2.2.0
The base of the code is a fork from the [official page](http://minisat.se/MiniSat.html).
## Build
This archive has fixed some issues/errors would occur on MacOS with native clang
```
Apple clang version 17.0.0 (clang-1700.0.13.5)
Target: arm64-apple-darwin24.6.0
Thread model: posix
InstalledDir: /Library/Developer/CommandLineTools/usr/bin
```
- [x] error: invalid suffix on literal; C++11 requires a space between literal and identifier [-Wreserved-user-defined-literal]
- [x] error: friend declaration specifying a default argument must be a definition

now
```bash
export MROOT=<minisat-dir>
cd core
make libr 
```
will be good to go.

## Original README
```
================================================================================
DIRECTORY OVERVIEW:

mtl/            Mini Template Library
utils/          Generic helper code (I/O, Parsing, CPU-time, etc)
core/           A core version of the solver
simp/           An extended solver with simplification capabilities
README
LICENSE

================================================================================
BUILDING: (release version: without assertions, statically linked, etc)

export MROOT=<minisat-dir>              (or setenv in cshell)
cd { core | simp }
gmake rs
cp minisat_static <install-dir>/minisat

================================================================================
EXAMPLES:

Run minisat with same heuristics as version 2.0:

> minisat <cnf-file> -no-luby -rinc=1.5 -phase-saving=0 -rnd-freq=0.02
```
