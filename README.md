# deno-loader
A ECMAScript Implementation of partial deno tooling and loader API's Allows to load the same code in different WInterOP Runtimes, and even build it for more Runtimes. 

## Why?
Deno is the most best Loader Builder Implementation on top of v8 but it also is for the most coders that target nodejs
a Additional Target. So To make Deno Land Code and ECMAScript written targeting Deno run able on other Platforms like
AwesomeOS or Chromium even NodeJS this is the Smallest Denominator. 

All ECMAScript Engines are not aware of any FileSystem API's they only know that they need to call the fetch implementation
If you use the import Operator or the dynamic import() function. The Rest is up to the Implementer

so fetch is the only real Interface that is defined by ECMA to get code into the Engine via Code Instructions. 

The secund way to get something into the Engine is the load function if it exists it is able to dynamical load 
asm modules or other modules and link them into the stack.

