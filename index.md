---
layout: default
---

<div align="center">
    <img src="https://raw.githubusercontent.com/LGala/Icaro/main/images/logo.jpg" width="35%" >
</div>

# The Icaro philosophy

Icaro is a JVM programming language born as a didactic project with a great ambition in the long run: be a full JVM language (like Java/Kotlin) baked into a more pragmatic/easy ecosystem (Rust, Go, JavaScript, Python) and avoid the typicals complexities of the JVM ecosystem (complex setups into IDEs like Intellij/Eclipse, complex or ugly packet managers like Maven, Gradle).

# What it's able to do

At the moment it's only able to:
* assign math expressions* to variables
* assign the value of a variable A to variable B
* print math expressions* and variables content to the screen

##### for example**

```bash
a = 10 * 2

b = -a * -2

print (a + b) / 60
```

###### *More specifically these expressions are made of integers, the 4 basic math operators and round parenthesis only. For other info take a look at the language grammar.

###### **Icaro doesn't accept white spaces after the statements (if you don't know what a statment is, `print 1` and `a = 2` are statements) and newlines after the last statement. I know it's annoying and this kind of behaviour will be tossed away in the next releases.

# Getting started

## Prerequisites

* JDK 11+
* bash or zsh shell

## Installation

##### bash users

```bash
wget https://raw.githubusercontent.com/Icaro-lang/compiler/main/installers/bashicaroinstaller.sh && bash bashicaroinstaller.sh && source ~/.bashrc; rm bashicaroinstaller.sh
```

##### zsh users

```bash
wget https://raw.githubusercontent.com/Icaro-lang/compiler/main/installers/zshicaroinstaller.sh && bash zshicaroinstaller.sh && source ~/.zshrc; rm zshicaroinstaller.sh
```

##### Go in any directory you want, and you should be able to launch the following command now

```bash
icaro .
```

##### And receive something like

```
available commands:
-compile: given the .icaro program, it creates the .class file
-run: executes the given the .class file
-compile-run: -compile and then -run
-compile-run-noclass generate and executes the bytecode without creating any .class files
<every other command>: print the available command list
```

##### Create your first program

```bash
mkdir playWithIcaro && cd playWithIcaro && echo "print -5 * (3 + 1) / 4" | tr -d '\n' > myFirstProgram.icaro;
```

##### Run the program

```bash
icaro -compile-run-noclass myFirstProgram.icaro
```

##### And receive

```
-5
```
