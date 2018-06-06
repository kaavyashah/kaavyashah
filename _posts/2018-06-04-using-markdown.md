---
layout: post
title: "Using Markdown"
---
---
## Headers
Header sizes are dependent upon the `#`s that come before the heading itself.

```
# Header 1

Alternative Header 1
---
## Header 2

Alternative Header 2
===
### Header 3
#### Header 4
##### Header 5

```
# Header 1

Alternative Header 1
---
## Header 2

Alternative Header 2
===
### Header 3
#### Header 4
##### Header 5
---
## Emphasis
```
*italics* or _italics_
**bold** or __bold__
**bold and _italicized_**
~~strikethrough~~
```
*italics* or _italics_

**bold** or __bold__

**bold and _italicized_**

~~strikethrough~~

---
## Quoting Text
To quote text, you can use a `>`
```
This is meant to show
> how to quote Text
```
This is meant to show
> how to quote Text

---
## Quoting Code
For inline `code` simply put `backticks` around the words.
```
For inline `code` simply but `backticks` around the words.
```
Full blocks of code can work for specific languages or none at all.  In terms of the example,
`java` can be replaced with `javascript` accordingly.

{% highlight ruby %}
```java
var s = "Java syntax";
func(s);
```

```python
s = "Python syntax"
print s
```

```
No language indicated
```
{% endhighlight %}

```java
var s = "Java syntax";
func(s);
```
```python
s = "Python syntax"
print s
```
```
No language indicated
```

---
## Lists
Unordered lists can be created using `-` or `*`.  To create nested lists, indent
all items underneath the desired line.
```
- one thing
* another thing
  * another thing
```
- one thing
* another thing
  * another thing

To create numbered lists, put a number at the beginning of each line.

```
1. First
2. Second
3. Third
```

1. First
2. Second
3. Third

### Task Lists

```
- [x] This is completed
- [ ] This is incomplete
- [ ] Let's just throw another in
```
- [x] This is completed
- [ ] This is incomplete
- [ ] Let's just throw another in

---
### Arrows
* `&uparrow` = &uparrow
* `&downarrow` = &downarrow
* `&leftarrow` - &leftarrow
* `&rightarrow` = &rightarrow
