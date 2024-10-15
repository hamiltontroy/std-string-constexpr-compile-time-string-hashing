In c++ as of c++ 23 we dont have compile time hashing, meaning a "switch case" statement
will not work on hashed strings. Ive tried a bunch of other options, such as a global
constructor that calls std::hash on a list of strings, that does not work because
its not compile time. Ive tried using hash maps during runtime, that works but is
disgusting and janky to deal with. This seems like the best option to me.

It is a nice solution, but everytime you want to add a url option to your site,
you need to recompile the entire program, so keep that in mind.

It is super nice to just have a "switch case" for certain situations.

This program will read from an input file, and then generate c++ code
with a bunch of const std::size_t variables assigned to the hash of your string.

E.g. just look at the examples, they are like 7 lines of code.
