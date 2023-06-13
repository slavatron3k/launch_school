# Introduction to Programming with Ruby

## Getting Started

### Introduction

#### Computer Science and Layers of Abstraction
* **Domain Specific Language (DSL)**
    * e.g. **Rails** and **Rspec**

### Preparations

#### Reading Documentation
* "::" denotes **namespace**
    * All classes belong in a namespace
* ::class_method
    * Public Class **Methods** are called directed from the **class**
* #instance_methods
    * Public Instance Methods can be applied to any instance of the class
* Classes can have parents
* Included **modules** add functionality available to classes
* Documentation will be used extensively over one's programming career

#### Using the Command Line and irb
* Ruby offers an interactive coding environment named **irb**

#### What Are Ruby "Gems"?
* **Gems** are a collection of Ruby files, or a Ruby **library**
* The publishing system behind organizing, listing, and publishing those libraries, or gems
* Ruby gems are versioned based off the **Semantic Versioning** standard
* Gems can be installed manually or managed centrally from the **Gemfile**

#### Debugging Ruby Code with Pry
* **Pry** is a gem that serves as an alternative to irb and offers great debugging features
    * `require "pry"` and `binding.pry` are needed

## Intro to Programming

### The Basics

#### Literals
* A **literal** represents a fixed value or constant in the source code

#### Strings
* **Strings** represent text data
    * `"This is a string."`
    * Single and double quotes are used to define a string literal
        * Double quotes allow for **string interpolation** which **concatenates** Ruby code with a string
            * `#{ruby expression goes here}`
    * The backslash or **escape character** communicates to the computer that quotes that follow it are not to be interpreted as syntax

#### Symbols
* A **symbol** is used in reference to a string that will never be printed or manipulated
    * They are denoted `:symbol_name`

#### Numbers
* Numbers are represented via **integers** and **floats**
    * Integer e.g. `1`
    * Floats are fractional whereas integers are not
        e.g. `1.1`

#### Nil
* Nil represents nothing or empty
    * `nil`
    * A thing can be checked as `nil` with `.nil.`
    * It can be used as a **conditional** and evaluates to **`false`**

#### Operations
* Addition: `1 + 1` evaluates to `2` 
* Subtraction: `1 - 1` evaluates to `0`
* Multiplication: `1 * 1` evaluates to `1`
* Division: `1 / 1` evaluates to `1`
* **Modulo**: `5 % 4` evaluates to `1`
    * The number left of the percent sign is the **dividend** and the number right of the percent sign is the **modulus**
    * "Modulo operations return a positive integer when the second operand is positive and a negative integers when the second operand is negative."
    * "Remainder operations return a positive integer when the first operand is positive, and a negative integers when the first operand is negative"
* Floats: `15.0 / 4` evaluates to `3.75`, `9.75 * 4.32` evaluates to `42.120000000000005`
    * As long as an evaluated expression contains one float, then a float will be returned
* Equality: `1 == 1` evaluates to `true`, `1 == 2` evaluates to `false`, `'hello' = 'hello'` evaluates to `true`, `'hello' === world'` evaluates to `false`
    * Statements of equality evaluate the **boolean** relationship between objects
        * Boolean values: `true`, `false`
* String concatenation: `'hello'` + `'world'` evaluates to `'hello world'`

#### Type Conversion
* To integer: `to_i`
    * `'1'.to_i` evaluates to `1`
* To float: `to_f`
    * `'1.1'.to_f` evaluates to `1.1`
* To string: `to_s`
    * `1.to_s` evaluates to `'1'`

#### Basic Data Structures
* **Arrays**
    * Arrays store any data types into ordered lists
        * e.g. `[1, 2, 3, 4, 5]` evaluates to `[1, 2, 3, 4, 5]`
    * An **index** refers to a specific position in an array and start from `[0]`
        * e.g. `[1, 2, 3, 4, 5][0]` evaluates to `1`
* **Hashes**
    * A **hash** or dictionary is a set of **key-value pairs**
    * It associates a key (in the form of a symbol) with a value of any data type
        * e.g. `{:hog => 'squeals'}` evaluates to `{:hog => 'squeals'}`, `{:hog => 'squeals', :horse => 'neighs'}` evaluates to `{:hog => 'squeals', :horse => 'neighs'}`
    * A value of a hash can be retrieved with the associated key
        * `{:hog => 'squeals', :horse => 'neighs'}[:hog]` evaluates to `'squeals`

#### Expressions and Return
* A **hash-rocket** `=>` precedes a returned value
* An **expression** is anything that can be evaluated
    * Expressions always return a value

#### Puts vs. Return
* `puts` prints to the screen, but does not return what is printed
    * e.g. `puts 'hello'` evaluates to `nil` while `'hello'` is printed to the screen