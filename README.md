# Snake

Oh my goodness. Who could have known that you can do interesting things with
a functional programming language? I surely didn't!

Implementation of Snake in Clojure.

This is me playing around with Clojure, specifically getting used to how 
game state could be handled with mutable data through ```refs``` and ```transactions```.

I also dove into the deep-end without my lifejacket as I moved away from using vim. I was using
[emacs](https://www.gnu.org/software/emacs/) with [CIDER](https://cider.mx/).
My initial assessment of emacs is that it is a wonderful environment for
programming in lisp-y dialects. However, I am still so much faster with vim
while using another terminal as the repl.

## How to Play
The goal of the game is to grab 15 apples (represented as red bars that are randomly
generated on the board) with your snake (represented as a long green bar that
grows every time you eat an apple). You control your snake with your arrow keys
and the goal is to not collide with your own body.

![snake-1](https://github.com/anthonygraca/snake/blob/main/screenshots/snake-1.png)
![snake-2](https://github.com/anthonygraca/snake/blob/main/screenshots/snake-2.png)

## How to Build and Run
### Clojure Code with Leiningen
[Leiningen](https://leiningen.org) is the build tool that manages all of the
Clojure code in this project. Code runs on a JVM environment so Java is
required.

Instructions on how to [install Clojure](https://clojure.org/guides/getting_started).

### Inital Setup 
1.) Grab the lein installation script
```
wget https://raw.github.com/technomancy/leiningen/stable/bin/lein
```
2.) Make script into a executable
```
chmod +x lein
```
3.) Move lein script into a location accessible in $PATH
``` 
mv lein ~/bin
```
4.) Checkout this snake code base
```
git clone git@github.com:anthonygraca/snake.git
```
5.) Change directory into repo
```
cd snake
```
6.) Run lein
```
lein run 
```

## What Amazed Me
- This game was just written with ~120 lines of clojure code and most of the
  pure functions are TINY. Even the GUI portion is only around 15-20 lines of code.
- I am not a game programmer but whenever I try, I always have some
  ```while(true)``` statement that shoots my CPU utilization to 100%. In
  retrospect, it was probably because I am not using a proper game dev library.
  Also, this game is portable since it is on the JVM and it barely uses CPU
  and memory compared to what I was expecting!

## License

Copyright © 2021 Anthony Graca

This program and the accompanying materials are made available under the
terms of the Eclipse Public License 2.0 which is available at
http://www.eclipse.org/legal/epl-2.0.

This Source Code may also be made available under the following Secondary
Licenses when the conditions for such availability set forth in the Eclipse
Public License, v. 2.0 are satisfied: GNU General Public License as published by
the Free Software Foundation, either version 2 of the License, or (at your
option) any later version, with the GNU Classpath Exception which is available
at https://www.gnu.org/software/classpath/license.html.
