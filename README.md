# Shoctode

*A graphical shell for the current millenium.*
Currently conceptual.

Shoctoe is a flow based programming interface,
for live programming.
Itprovides a real time preview of all data and graphical
tools to build custom GUIs.
Shoctode is based on the functional programming language
**to be decidet**.
The objective of Shoctode is to provide a
*current-millenium* replacement for the CLI, while sticking
to the core concepts of UNIX: *Do one thing well*.
In spite of the UNIX shell it's based on the functional
programming language **to be decidet**, which is used for
all the libbrarys and the code generation.

## Intro

At the moment there are basically two ways to interact with
a computer: Text for the programmers and unix veterans and
GUI for the mere user. Both approaches have huge advantages:
With a GUI huge amounts of highly complex data can be
displayed while the text interface provieds the power of a
programming language.

Shoctode aims at merging those concepts int a single,
programmable user interface.

## Lang

Shoctode requires a programming language (duh) and runtime,
which should provide the following features:

* Interpreted execution
* Native compiling
* AST export with reflection
* AST back conversion
* Strong type system
* Functional programming

The candidates are currently:

* Erlang
* OCaml
* Haskell
** We could use the types

## The Flow

Shoctode is written (and translates to) a functional
language. Most of the functional concepts will be
preseserved (functions are just types, no side effects).
The main difference will be, that the flow based style
supports multiple return value, these can however be easily
implemented by using tuples/structures as return value.

## Terminology

The following concepts of data flow programming shall map
directly to their functional pendants:

* *Node -> Function*
* *Pipe -> Data*, connections between nodes
* *Input -> Arguments*
* *Output -> Return value*, expressed as a structure/tuple
  if more than one

## Sec

Each application shall be run by default in a no acess
jail. This jail restricts access to (at least) the following
resources:

* Syscalls in general
* FS
* Network
* Processes
* Sockets
* Memory
* CPU Time
* Process creation
* Windows/Graphics
* Devices
* Input

The jail shall posess the ability to:

* Deny access
* Modify access/output (e.g. `$ ls /` gives
  'this_is_virtual.txt')
* Allow access

Default restriction for all IO, and proocess management is to deny acess.
Default for Memory/CPU Time is to allow a certan load.
It is always possible to create a custom enviroment ("modify
access") without restriction.

Jailing is done through access tokens, which can be modified
to drop certain priviliges.

Elevating access shall only be posible by using
cryptographic keys to sign access tokens.
These tokens shall also be the *root* of all permissions.

Where possible real cryptographic protection (e.g. Hard
Drive Encryption) shall be used instead of access control
(e.g. Full Disk Encryption instead of FS Permissions).

## To think about

Put stuff here we need to integrate into the sections above.

* I dont have anything right now,
* but this is a Ãlist and a topic could look like
* Joy and Play 
