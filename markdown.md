## Markdown Guide (মার্কডাউন গাইড )

মার্কডাউন তৈরি করেছে John Gruber. মার্ক ডাউন ব্যবহার করে খুব সহজে নোট, ডকুমেন্টেশন ইত্যাদি লেখা যায়। 
# 1 Heading 
to make heading use "#", ex one # is for h1
```md
# Heading H1
## Heading H2...
###### Heading H6
```
#### Example:-

# Heading H1
## Heading H2
###### Heading H6

# 2 Paragraph
```md
Simple Text are used for writnig paragraph.
```
#### Example:-
Simple Text are used for writnig paragraph. Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.

Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.Simple Text are used for writnig paragraph.

# 3 Image
```md
![Image Alternative Name](url, like: ls-l.png)
```
#### Example:-
![linux file listing](ls-l.png)

# 4 Link
```md
[Mobarok github profile](https://github.com/mobaarok)
```
#### Example:-
[Mobarok github profile](https://github.com/mobaarok)


# 5 Code Block
to make code bolck use three "```" or "~~~" . and end it also
```md
```js
const getName = (param) => {
  echo "Mobarok Hossain";
}
` ` `
```

#### Example:-
```js
const getName = (param) => {
  echo "Mobarok Hossain";
}
```

# 6 List
use "-" or "*" for make list, and use 4 space to make nasted list

## Ordered List
```md
- Bulleted
- List
  - nested
  - list
  
```
#### Example:- 
- Bulleted
- List
  - nested
  - list

## Unordered List
```md
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

#### Example:-
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b


# 7 Inline Code Block
```md
this is inline `ctrl+del` code block example
```
this is inline  (`ctrl+del`) code block example 

# 8 Bold & Italic
```md
**Bold** and _Italic_ and `Code` text
```

**Bold** and _Italic_ and `Code` text

## 8.1 to make Bold and italic at once

```md
** _ This is italic and bold _ **
*This text will be italic*
_This will also be italic_
**This text will be bold**
__This will also be bold__
_You **can** combine them_
```

#### Example:-
**_This is italic and bold_**

*This text will be italic*

_This will also be italic_

**This text will be bold**

__This will also be bold__

_You **can** combine them_

# 9 Blockuote

```md
> We're living the future so
> the present is our past.
```
#### Example:-
> We're living the future so

> the present is our past.

# 10 Some more style

```md 
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```
#### Examlpe:- 

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

# 11 Table
```md
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```
#### Example:-
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column