---
layout: post
title: Jekyll Tips
---
### Heading Size
Usually, 1 hash preceding the header is the largest size, but for the purposes of jekyll
use 2 to create the largest header.

For example, use the following as the headers:
```
## Second
### Third
#### Fourth
##### Fifth
```
## Second
### Third
#### Fourth
##### Fifth

---
### Block Code
For jekyll specifically, blocks of code can be shown by beginning a block with `{ % highlight ruby % }`
and ending the block with `{ % endhighlight % }`. When actually typing, remove the space between the
`{` and `%` and the `%` and `}`.
```
{ % highlight ruby % }
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{ % endhighlight % }
```
{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}
