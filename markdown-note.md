# Markdown Tutorial

### Markdown Guide \(মার্কডাউন গাইড \)

মার্কডাউন তৈরি করেছে John Gruber. মার্ক ডাউন ব্যবহার করে খুব সহজে নোট, ডকুমেন্টেশন ইত্যাদি লেখা যায়।

## 1 Heading

to make heading use "\#", ex one \# is for h1

```text
# Heading H1
## Heading H2...
###### Heading H6
```

#### Example:-

## Heading H1

### Heading H2

**Heading H6**

## 2 Paragraph

```text
Simple Text are used for writnig paragraph.
```

#### Example:-

Simple Text are used for writnig paragraph. Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.

Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.

## 3 Image

```text
![Image Alternative Name](url, like: ls-l.png)
```

#### Example:-

![linux file listing](https://github.com/mobaarok/markdown/tree/dd4d25077f67eff7c4ec15a99a95a6e68a50e332/ls-l.png)

## 4 Link

```text
[Mobarok github profile](https://github.com/mobaarok)
```

#### Example:-

[Mobarok github profile](https://github.com/mobaarok)

## 5 Code Block

to make code bolck use three "\`\`\`" or "~~~" . and end it also

```text
```js
const getName = (param) => {
  echo "Mobarok Hossain";
}
` ` `
```

#### Example:-

```javascript
const getName = (param) => {
  echo "Mobarok Hossain";
}
```

## 6 List

use "-" or "\*" for make list, and use 4 space to make nasted list

### Ordered List

```text
- Bulleted
- List
  - nested
  - list
```

#### Example:-

* Bulleted
* List
  * nested
  * list

### Unordered List

```text
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

#### Example:-

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

## 7 Inline Code Block

```text
this is inline `ctrl+del` code block example
```

this is inline \(`ctrl+del`\) code block example

## 8 Bold & Italic

```text
**Bold** and _Italic_ and `Code` text
```

**Bold** and _Italic_ and `Code` text

### 8.1 to make Bold and italic at once

```text
** _ This is italic and bold _ **
*This text will be italic*
_This will also be italic_
**This text will be bold**
__This will also be bold__
_You **can** combine them_
```

#### Example:-

_**This is italic and bold**_

_This text will be italic_

_This will also be italic_

**This text will be bold**

**This will also be bold**

_You **can** combine them_

## 9 Blockuote

```text
> We're living the future so
> the present is our past.
```

#### Example:-

> We're living the future so
>
> the present is our past.

## 10 Some more style

```text
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

#### Examlpe:-

* [x] @mentions, \#refs, [links](markdown-note.md), **formatting**, and ~~tags~~ supported
* [x] list syntax required \(any unordered or ordered list supported\)
* [x] this is a complete item
* [ ] this is an incomplete item

## 11 Table

```text
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```

#### Example:-

| First Header | Second Header |
| :--- | :--- |
| Content from cell 1 | Content from cell 2 |
| Content in the first column | Content in the second column |

