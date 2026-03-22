---
{"dg-publish":true,"permalink":"/javascript-templating-benchmark/","tags":["programming","javascript"],"created":"2011-05-23"}
---


There are many popular libraries to do templating in Javascript.

The most popular are:

-   [JQuery Template](http://api.jquery.com/jQuery.template/)
-   [Pure Template](http://www.javascriptr.com/2008/06/05/purejstemplate-a-pure-javascript-templating-engine-for-jquery/)
-   [Resig Template](http://ejohn.org/blog/javascript-micro-templating/)
-   [Trimpath Template](http://code.google.com/p/trimpath/wiki/JavaScriptTemplates)
-   [JQote2 Template](http://aefxx.com/jquery-plugins/jqote2/)

I decided to benchmark them, so I created a simple \"hello world\" test. You can find it [here](file:///junk/js/tmpl.html).

As usual, the results are interesting. Here are, on my box:

```{=html}
<table>
<tr>
<th></th>
<th>
```
Firefox 3.6

```{=html}
</th>
<th>
```
Chrome 11.0

```{=html}
</th>
<th>
```
Safari 5.0

```{=html}
</th>
</tr>
<tr>
<td>
```
JQuery Template

```{=html}
</td>
<td>
```
297ms

```{=html}
</td>
<td>
```
138ms

```{=html}
</td>
<td>
```
113ms

```{=html}
</td>
</tr>
<tr>
<td>
```
Pure

```{=html}
</td>
<td>
```
309ms

```{=html}
</td>
<td>
```
43ms

```{=html}
</td>
<td>
```
36ms

```{=html}
</td>
</tr>
<tr>
<td>
```
Resig

```{=html}
</td>
<td>
```
309ms

```{=html}
</td>
<td>
```
41ms

```{=html}
</td>
<td>
```
41ms

```{=html}
</td>
</tr>
<tr>
<td>
```
Trimpath

```{=html}
</td>
<td>
```
15ms

```{=html}
</td>
<td>
```
5ms

```{=html}
</td>
<td>
```
6ms

```{=html}
</td>
</tr>
<tr>
<td>
```
JQote2

```{=html}
</td>
<td>
```
7ms

```{=html}
</td>
<td>
```
1ms

```{=html}
</td>
<td>
```
6ms

```{=html}
</td>
</tr>
</table>
```
A part from the obvious result that Firefox is the slowest browser of all, I\'m astonished by the excellent performance of JQote2!
