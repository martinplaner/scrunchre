scrunchre
=========

Simple wordlist generator that takes a regex pattern and generates all possible word combinations.

Currently only very simple regular expressions are supported.

__Supported stuff__
* Bracket expressions (e.g. "[A-z]", "[a-z]", [asjfh.,], "[0-9]", etc.)
* Character literals (e.g. "hello"; although somewhat useless on its own ;)
* Cardinality expressions (e.g. "[abc]{1,3}")
* Options (e.g. "ab?", "a[bc]?")

Known Bugs
----------

Lots and lots of them. But the tool currently works for me and this is good enough for me to not tinker with it at the moment.
So don't be suprised if it crashes or freezes on you.

One word of advice: Do not use `+` or `*` in your expression as this will try to generate word combinations up a length of `INT_MAX` (i.e. will crash/freeze).

Examples
--------

* scrunchre.py "abc?"

```
    ab
    abc
```

* scrunchre.py "[A-z]{1,3}[0-9]{2}"

```
    A00
    A01
    ...
    zzz98
    zzz99
```
* scrunchre.py "hell[oO]\?"
    
```
    hello?
    hellO?
```
