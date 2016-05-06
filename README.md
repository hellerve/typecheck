# typeinfer

A simple and naive type inference library for zepto code.

## Usage

![](http://g.recordit.co/QC7E2Z5Cvw.gif)

```
(load "typeinfer")
(import-all "typeinfer")
(typeinfer:infer-program some-program)
(typeinfer:infer-expression some-expression)
```

## Caveats

This library does not about currying, overloading
or generic functions. If it is determined that
the function works on integers, the typeinferer
will assume this a truth. If later facts disprove that
claim, it will just assume the thing is `:ambiguous`,
which it is.

Also, there are almost no primitives in the initial
environment, so a lot of functions might seem
`:unbound` when in reality they are just a part
of the standard library.

<hr/>

Have fun!
