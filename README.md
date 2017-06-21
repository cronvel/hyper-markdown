
# Hyper-Markdown

This is a markdown superset, providing extra syntax.

This contains *original markdown* + *GFM* + *specific Hyper-Markdown syntax*.

**Note:** This package is built on top of a fork of [Christopher Jeffrey's marked](https://github.com/chjj/marked) (MIT license).



## Why another Markdown extension?

The objective of **Hyper-Markdown** is *zero HTML for content*.

Markdown, especially with the *GFM extension*, almost reached this goal,
but there are still few common cases where HTML is still necessary.



## Specific Hyper-Markdown syntax

* Block markup (at the begining of a line):
	* `!![caption](url)` create a *figure* (block) tag containing an image or a media having *url* as source,
	  it uses the text inside brackets as content for a *figcaption* tag
	* `:!![caption](url)` same, but make the *figure* float to the left (i.e. give it classes *float* and *float-left*)
	* `!!:[caption](url)` same, but make the *figure* float to the right (i.e give it classes *float* and *float-right*)
	* `|||` column break
	* `+++` (or `+ + +` or `++++++++` or anything following the horizontal rule syntax) are used as *section break*:
	  it clears all columns and start over on a fresh one-column section
	* `- [ ] ` or `* [ ] ` or `+ [ ] ` introduce a todo list item
	* `- [x] ` or `* [x] ` or `+ [x] ` introduce a todo list item done



## Renderer object API

New methods / modified methods of **marked** module:

* .media( type , href , caption , float )
* .startSection( columnDepth )
* .endSection( columnDepth )
* .startColumn( columnDepth )
* .endColumn( columnDepth )
* .list( body , ordered , todoList )
* .listitem( text , checkbox )

