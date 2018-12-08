---
layout: default
---

# How to use Markdown

The following markdown formatting can be used to create new pages for this website

---

## Text
```
**bold**
```
**bold**
```
_italic_
```
_italic_
or
```
~~strikethrough~~
```
~~strikethrough~~

Links are formatted as the following:

```
[Link to another page](./another-page.html)
```

[Link to another page](./another-page.html)

---

## Headers and block quotes

```
# Header 1

This is a normal paragraph following a header.

## Header 2

> This is a blockquote following a header
>
> This is the end of the block quote.

### Header 3

#### Header 4

##### Header 5

###### Header 6

```

# Header 1

This is a normal paragraph following a header.

## Header 2

> This is a blockquote following a header
>
> This is the end of the block quote.

### Header 3

#### Header 4

##### Header 5

###### Header 6

---

## Code

Use the language after the 3 tickmarks for syntax highlighting:

```
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
```

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
```
```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

## Lists

```
*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.
```

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.


## Ordered Lists

```
1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.
```
1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.



## Table Example

```
| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |
```
| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |


## Horizontal Rule
```
* * *
```
* * *


## Nested list:
```
- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item
```

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

## Small image

```
![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)
```

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

## Large image

```
![Branching](https://guides.github.com/activities/hello-world/branching.png)
```

![Branching](https://guides.github.com/activities/hello-world/branching.png)


## Definition lists can be used with HTML syntax.

```
<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>
```

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

* * *
