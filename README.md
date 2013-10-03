up
==

Requirement
-----------

- Ruby (`up` is a simple Ruby one-liner)

Install
-------

```shell
wget -O /usr/bin/up https://raw.github.com/woongy/up/master/up
```
and then add `alias up="source /usr/bin/up"` to `.bashrc` and/or `.bash_profile`


Usage
-----

- Jump to the nearest parent directory

        /foo/bar/baz/qux $ up foo
        /foo $


- Case-insensitive match by default

        /fOo/bar/baz/qux $ up FoO
        /foo $

- Match by first characters

        /foo/bar/baz/qux $ up fo
        /foo $

- `up` with no arguments works like `cd ..`

        /foo/bar/baz/qux $ up
        /foo/bar/baz $


Known Issues
------------

- `up` to `/` does not work (but we already have `cd /` for that)

        /foo $ up /     # error
        /foo $ up       # stays at /foo
