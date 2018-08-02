# C++ Style Guide

A style guide for C++, still work in progress. I found several
[other](https://github.com/bbatsov/ruby-style-guide)
[style](https://github.com/polarmobile/coffeescript-style-guide)
[guides](https://github.com/bbatsov/clojure-style-guide) on Github, but not one for C++. So I've created this as a
starting point. Feel free to create an issue or a pull request.

## Source Code Layout

* Use UTF-8 as the source file encoding
* Use Unix-style line endings.
	* If you're using Git you might want to add the following
	  configuration setting to protect your project from Windows line
	  endings creeping in:

		`git config --global core.autocrlf true`
* Use Tabs for indentation and spaces for alignment.

## Naming

CamelCase for types, camelCase for names.

```cpp
class Example {
public:
	void fooBar(int firstVar, int secondVar) {
		for (int i = 0; i < 10; ++i) {
			std::cout << i << std::endl;
		}
	}
};
```

## Local includes before system ones

```cpp
#include "thisfile.hpp"

#include "a.hpp"
#include "b.hpp"

#include <iostream>
```

## Only use `/* */` within one line

To comment multiple lines prepend them with `//`.

```cpp
void foo(int /*unused*/) {
	// 1
	// 2
	// 3
}
```

The reason for this is that many line-based tools (e.g. merging with Git or `git blame`) won't know that a `/*` also affects the following lines.
