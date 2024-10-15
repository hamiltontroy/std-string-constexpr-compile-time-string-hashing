# Compile Time String [Hashing](https://en.wikipedia.org/wiki/Hash_function) in C++

## Why is it the best

In C++ as of C++ 23 we dont have compile time [Hashing](https://en.wikipedia.org/wiki/Hash_function), meaning a [Switch Statement](https://en.wikipedia.org/wiki/Switch_statement)
will not work on hashed strings. Ive tried a bunch of other options, such as a global
consstructor that calls [std::hash](https://en.cppreference.com/w/cpp/utility/hash) on a list of strings, that does not work because
its not compile time. Ive tried using hash maps during runtime, that works but is
disgusting and [janky](https://www.urbandictionary.com/define.php?term=janky) to deal with. This seems like the best option to me.

It is a nice solution, but everytime you want to add a [url](https://datatracker.ietf.org/doc/html/rfc1738) option to your site,
you need to recompile the entire program, so keep that in mind.

It is super nice to just have a [Switch Statement](https://en.wikipedia.org/wiki/Switch_statement) for certain situations.

## How it works and How to Use

This program will read from an input file, and then generate c++ code
with a [const](https://learn.microsoft.com/en-us/cpp/cpp/const-cpp?view=msvc-170) [std::size_t](https://en.cppreference.com/w/cpp/types/size_t) variables assigned to the hash of your string.

E.g. just look at the examples, they are like 7 lines of code.
