# deno-loader
A ECMAScript Implementation of partial deno tooling and loader API's Allows to load the same code in different WInterOP Runtimes, and even build it for more Runtimes. 

## Why?
Deno is the most best Loader Builder Implementation on top of v8 but it also is for the most coders that target nodejs
a Additional Target. So To make Deno Land Code and ECMAScript written targeting Deno run able on other Platforms like
AwesomeOS or Chromium even NodeJS and es4x / GraalJS on GraalVM, this is the Smallest Denominator. 

All ECMAScript Engines are not aware of any FileSystem API's they only know that they need to call the fetch implementation
If you use the import Operator or the dynamic import() function. The Rest is up to the Implementer

so fetch is the only real Interface that is defined by ECMA to get code into the Engine via Code Instructions. 

The secund way to get something into the Engine is the load function if it exists it is able to dynamical load 
asm modules or other modules and link them into the stack.

the 3rd way is the fact that near any common Engine implements FileSystem API's and this https://github.com/lemanschik/native-file-system-adapter provides the needed unifed Adapter for that

## What does it solve?
- Binary Snapshoots for supported Runtimes: Deno, Chromium, NodeJS, B8G, V8
- Packaging Bundling for supported Runtimes
- Load and Transform Hooks.
- Solutions to common Problems when dealing with legacy Code.
- Works also for Deno to Add extra functionality that deals with legacy Code and Projects as also Packages.
- Is used by B8G as the Main loader and Build System.
- Does Replace a Common used Package Manager when this Project reaches 1.0
- Will Use the Universal OPFS API's Like StorageManager and Polyfill them if needed.
  - https://github.com/lemanschik/native-file-system-adapter

## Goals
Code Once for deno and let it run anywhere even on targets like cloudflare workers and NGINX NJS or your Local Browser
but Mainly this is a Core Part of AwesomeOS to make it more easy to integrate legacy Software and Optimize it Incremental.

also inhires the server parts for widly known cdn's and ECMAScript Package Processing pipelines like git, npm, esm.sh which uses esbuild, unpkg.com which is mainly a call fetch pattern over npm.


