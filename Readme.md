# Rumi - a "toy" compiler

> Everything you possess of skill, and wealth, and handicraft, wasn't it first merely a thought and a quest? - Rumi

Rumi is a WIP compiler, that's all there is to it.

# How to compile the compiler?

Install `llvm (>=8.0)`, `bison` and `flex` then run make.

# How to compile using the compiler?

Run `./rum test.rum` and then do `gcc out.o lib.c`, your compiled file is available at `a.out`.

As a shortcut, you can run `make test`.

# How to debug?

As of now, `rumi` is just a proof of concept. There is almost no error reporting and every feature is experimental. If you ever ran into any problem, while coding in `rumi` or while developing it, try these:

## See if LLVM has anything to say.

Run `./rum test.rum > test.ll` followed by `lli test.ll`.

## See what gdb has to say

Run `gdb rum` followed by `run test.rum`. You can try the following commands:

* `break classname::methodname`
* `break filename lineno`
* `bt` (back trace)
* `print EXPR` (prints value of EXPR)

# Current Language Features:

* Variables
* Functions
* Expressions
* Varargs
* String literals
* if else
* while

# Top Priority Language TODO list

* structs
* better vararg support
* pointers
* better array support

# Current Compiler TODO list:

* Add rumi executable that allows interpreting `.rum` files (instead of compiling)
* Add compiler flag support (`-o` for example)
* Allow multiple file compile at the same time
* Integrate linker into the compiler
