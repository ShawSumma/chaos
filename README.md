# Chaos

<p align="center">
  <img src="https://chaos-lang.org/img/chaos_logo.png" alt="Logo" height="300px"/>
</p>

<p align="center">
    Turn chaos into magic!
</p>
<p align="center">
    <img alt="GitHub Last Commit" src="https://img.shields.io/github/last-commit/chaos-lang/chaos?logo=GitHub&style=flat-square">
    <img alt="GitHub Commit Activity" src="https://img.shields.io/github/commit-activity/m/chaos-lang/chaos?logo=GitHub&style=flat-square">
    <a href="https://github.com/chaos-lang/chaos/blob/master/LICENSE">
        <img alt="GitHub License" src="https://img.shields.io/github/license/chaos-lang/chaos?logo=GitHub&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Linter+Checks%22">
        <img alt="GitHub Workflow Linter Checks Status" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Linter%20Checks?logo=GitHub&label=linter%20checks&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Automated+Tests%22">
        <img alt="GitHub Workflow Automated Tests Status" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Automated%20Tests?logo=GitHub&label=automated%20tests&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Memory+Leak+Checks%22">
        <img alt="GitHub Workflow Memory Leak Checks" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Memory%20Leak%20Checks?logo=GitHub&label=memcheck&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Memory+Sanitizer%22">
        <img alt="GitHub Workflow Memory Sanitizer" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Memory%20Sanitizer?logo=GitHub&label=memory%20sanitizer&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Address+Sanitizer%22">
        <img alt="GitHub Workflow Address Sanitizer" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Address%20Sanitizer?logo=GitHub&label=address%20sanitizer&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Undefined+Behavior+Sanitizer%22">
        <img alt="GitHub Workflow Undefined Behavior Sanitizer" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Undefined%20Behavior%20Sanitizer?logo=GitHub&label=undefined%20behavior%20sanitizer&style=flat-square">
    </a>
    <a href="https://github.com/chaos-lang/chaos/actions?query=workflow%3A%22Chaos+C+Extension+Feature+Tests%22">
        <img alt="GitHub Workflow Chaos C Extension Feature Tests Status" src="https://img.shields.io/github/workflow/status/chaos-lang/chaos/Chaos%20C%20Extension%20Feature%20Tests?logo=GitHub&label=Chaos%20C%20Extension%20Feature&style=flat-square">
    </a>
    <a href="https://codecov.io/gh/chaos-lang/chaos">
        <img alt="Code Coverage (Codecov)" src="https://img.shields.io/codecov/c/github/chaos-lang/chaos?logo=Codecov&style=flat-square">
    </a>
</p>
<p align="center">
    Chaos is a strongly typed, dynamic yet compilable, test-oriented procedural programming language that achieves zero cyclomatic complexity.
</p>

### Influenced by

 - TypeScript's type safety
 - Python's syntax, modules and extensibility
 - JavaScript's cross-platform support
 - Ruby's loops and blocks, Rexx's `FOREVER` keyword
 - PHP's dedication to server-side
 - Haskell's pure functions
 - C's speed and interoperability
 - Go's standalone executables

### Featured Aspects

 - There are no control structures. (no `if..else`, no `switch..case`) Decision making only possible on function returns:
   ```ruby
    num def add(num x, num y)
        num z = x + y
    end {
        z == 8  : f1(),
        z > 10  : f2(),
        default : f3()
    }
   ```
 - A single unit test is enough to have 100% coverage on functions, always.
 - Warns you about untested functions in the executed program.
 - Detects possible runtime errors in compile-time.
 - Unique function call system that combines procedures with some aspects of functional programming paradigm.
 - No `while` or `when` keywords. Loops are mostly predetermined. Infinite loops can only be achievable through the `INFINITE` keyword.
 - There are `break` and `continue` statements but breaking a multiline loop inside a function is forbidden.
 - Single source of errors and unique exit codes for each one of them. So the errors are catchable by other programs.
 - Language's itself forces you to write less error-prone code.
 - Say goodbye to dependency conflicts with [Occultist](https://occultist.io/) dependency manager.
 - Eliminated segmentation fault possibility using strict memory management and predictions.
 - Simplest [C extension development](https://chaos-lang.org/docs/16_chaos_c_extensions_development) framework so far.

## Installation

Install the requirements:

```shell
make requirements
```

Compile the Chaos source:

```shell
make
```

Install the `chaos` binary system-wide:

```shell
make install
```

## Interpreter

### Interactive Shell

```shell
$ chaos
    Chaos Language 0.2.0 (Jan 20 2021 02:39:23)
    GCC version: 9.3.0 on linux
    Turn chaos into magic!

kaos> print "hello world"
hello world
kaos> exit
    Bye bye!
```

### Program File as Command-line Argument

**hello.kaos**:

```ruby
print "hello world"
```

```shell
$ chaos hello.kaos
hello world
```

## Compiler

```shell
$ chaos -c hello.kaos -o hello
Starting compiling...
Compiling Chaos code into build/hello.c
Compiling the C code into machine code...
Cleaning up the temporary files...

Finished compiling.

Binary is ready on: build/hello
$ build/hello
hello world
```

Run `chaos --help` to see more options.

## Uninstallation

You can uninstall the `chaos` binary and its C headers with:

```shell
make uninstall
```

## Useful Links

[**Language Reference**](https://chaos-lang.org/docs/03_comments)

[**Developing Chaos C Extensions**](https://chaos-lang.org/docs/16_chaos_c_extensions_development)

[**API Reference**](https://chaos-lang.org/docs/api)

[**Template for Chaos C Extension Developers**](https://github.com/chaos-lang/template)

[**Documentation Repository**](https://github.com/chaos-lang/chaos-lang.org)

[**Bug Tracker**](https://github.com/chaos-lang/chaos/issues)

[**Occultist Dependency Manager**](https://github.com/chaos-lang/occultist)

[**Contribution Guide**](https://github.com/chaos-lang/chaos/blob/master/CONTRIBUTING.md)

[**Code of Conduct**](https://github.com/chaos-lang/chaos/blob/master/CODE_OF_CONDUCT.md)
