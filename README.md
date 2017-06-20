
# Hyper-Markdown

This is a markdown superset, providing extra syntax.

This contains *original markdown* + *GFM* + *specific Hyper-Markdown syntax*.

**Note:** This package is built on top of a fork of [Christopher Jeffrey's marked](https://github.com/chjj/marked) (MIT license).



## Hyper-Markdown syntax

* Block markup (at the begining of a line):
	* `!![caption](url)` create a *figure* (block) tag containing an image having *url* as source, use the text
	  inside brackets as content for a *figcaption* tag
	* `~!![caption](url)` same but make the *figure* float to the left (i.e. give it classes *float* and *float-left*)
	* `!!~[caption](url)` same but make the *figure* float to the right (i.e give it classes *float* and *float-right*)
	* `|||` column break (TODO)



