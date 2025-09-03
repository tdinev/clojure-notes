# Introduction

This document describes how to set up a working environment for Clojure on Linux.

We will be using [NixOS](https://nixos.org/) (version 25.05)---a Linux distribution that, among other features, facilitates setting up your system in a declarative way.

Our editor of choice will be Emacs with Bozhidar Batsov's formidable configuration [Prelude](https://prelude.emacsredux.com/en/latest/).
(We will go through setting it up in the next chapter.)

What sets this document apart from most other Clojure guides or books is its attempt to outline the most up-to-date way of dealing with things in the Clojure realm.
Many of the (by the way, outstanding) books out there use tools like [Leiningen](https://leiningen.org/) or [Boot](https://boot-clj.github.io/), whereas currently a majority of the Clojurians recommend the Clojure CLI instead.
