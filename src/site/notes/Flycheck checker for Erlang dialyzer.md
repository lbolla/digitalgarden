---
{"dg-publish":true,"permalink":"/flycheck-checker-for-erlang-dialyzer/","tags":["programming","erlang","lisp","emacs"],"created":"2015-05-09"}
---


Emacs Erlang mode misses the definition of a [flycheck](http://flycheck.readthedocs.org/en/latest/) checker using [dialyzer](http://www.erlang.org/doc/man/dialyzer.html). Just add these lines to your `.emacs` to enable it:

<script src="https://gist.github.com/lbolla/c989096bbc0ba31bb834.js"></script>

I prefer to use it *after* the normal Erlang checker, so I define the following, too:

```lisp
(flycheck-add-next-checker 'erlang 'erlang-dialyzer)
```

Enjoy!
