### 1.Headers
~~~ 
# This is an <h1> tag
###### This is an <h6> tag
~~~
#### Output:
# This is an h1 tag
###### This is an h6 tag

### 2.Emphasis
~~~
*This text will be italic*  
_This will also be italic_  

**This text will be bold**  
__This will also be bold__  

_You **can** combine them_  
~~~
#### Output:
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

### 3.Lists

#### Unordered
~~~
* Item 1
* Item 2
  * Item 2a
  * Item 2b
 ~~~
 #### Output:
* Item 1
* Item 2
  * Item 2a
  * Item 2b
  
#### Ordered
~~~
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
~~~
#### Output:
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

### Images
~~~
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
~~~
#### Output:
![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
