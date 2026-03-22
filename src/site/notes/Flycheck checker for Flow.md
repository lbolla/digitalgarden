---
{"dg-publish":true,"permalink":"/flycheck-checker-for-flow/","tags":["programming","emacs","lisp","erlang"],"created":"2014-11-19"}
---


[Yesterday](https://code.prod.facebook.com/posts/1505962329687926/flow-a-new-static-type-checker-for-javascript/) Facebook open sourced [Flow](https://code.prod.facebook.com/posts/1505962329687926/flow-a-new-static-type-checker-for-javascript/), a static type checker for Javascript. If you use [Emacs](http://www.gnu.org/software/emacs/), you can use [Flycheck](http://flycheck.readthedocs.org/en/latest/) to check your .js files on the fly using Flow.

Here is the checker definition I use:

<script src="https://gist.github.com/lbolla/476a030ff2fe06445918.js"></script>

I prefer to use Flow *after* [gjslint](https://developers.google.com/closure/utilities/docs/linter_howto), so I define the following, too:

```lisp
(flycheck-add-next-checker 'javascript-gjslint 'javascript-flow)
```

I also wrote another [[Flycheck checker for Erlang dialyzer\|Flycheck checker]] if you are interested.

Enjoy!
