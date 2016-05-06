# typecheck

A simple and naive typechecker for zepto code.

## Usage

![](http://g.recordit.co/QC7E2Z5Cvw.gif)

```
(load "typecheck")
(import-all "typecheck")
(typecheck:check-program some-program)
(typecheck:check-expression some-expression)
```

## Caveats

This library does not about currying, overloading
or generic functions. If it is determined that
the function works on integers, the typechecker
will assume this a truth. If later facts disprove that
claim, it will just assume the thing is `:ambiguous`,
which it is.

Also, there are almost no primitives in the initial
environment, so a lot of functions might seem
`:unbound` when in reality they are just a part
of the standard library.

<hr/>

Have fun!
