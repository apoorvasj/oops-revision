<h2>Understanding collisions</h2>
Say, I have two functions in two different files:
in a.cpp

```cpp
void print(){
cout<<"Hello world.";
}
```

and in main.cpp

```cpp
void print(){
cout<<"You are within main.";
}
```

The programs are compiled individiually. But if a linker tries to link the two programs collision or naming conflict would occur. If both the functions with same name were in a single program, it would result in a compiler error.

<h2>Namespaces</h2>
<p>The solution to this is a namespace to remove disambiguity.</p>
<blockquote>When C++ was originally designed, all of the identifiers in the C++ standard library (including std::cin and std::cout) were available to be used without the std:: prefix (they were part of the global namespace). However, this meant that any identifier in the standard library could potentially conflict with any name you picked for your own identifiers (also defined in the global namespace). Code that was once working might suddenly have a naming conflict when you include a different part of the standard library. Or worse, code that compiles under one version of C++ might not compile under the next version of C++, as new identifiers introduced into the standard library could have a naming conflict with already written code. So C++ moved all of the functionality in the standard library into a namespace named std (short for “standard”).</blockquote>
<h2>Avoiding using namespace std</h2>
When you use using namespace std, you defeat the purpose of the above quote. You are declaring the entire namespace as std. So, if you had a function called void cout(), there would definitely be a collision if you also have cout<<"Text"!
<br>
<br>
<a href="https://www.learncpp.com/cpp-tutorial/naming-collisions-and-an-introduction-to-namespaces/"> source </a>
