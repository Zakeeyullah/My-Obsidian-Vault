## Look and Feel

- The Look and Feel of the Obsidian is managed from `Settings > Appearence`
- Here you will find a section for CSS Snippets. These are your Custom CSS for the Obsidian.

> - Note: I am not a CSS expert. These codes are from here and there. Sometimes ChatGPT😉

**The CSS snippets which are available in my Vault are**:

CSS Snippet | Purpose
--|--
Abbr-Hover| To Display the Abbreviations on Hover
Cards | An Addon for Dataview to display in Cards format
Classdef | Defining Custom CSS Classes
Color-Block | This is a way of taking Notes within Color Blocks
Custom | Here I put my Custom CSS. I have altered for Emphasis.
Embed | Some optimizations for embeds
Heading | The Headings are styled here
Image | Class Definitions for Image Alignments
Mermaid | Some optimizations for Mermaid Diagrams
Table | Some optimizations for Tables 



### Abbr-Hover

- The below code snippet will show United Nations when hovered on UN

```md
<span title="United Nations">UN</span>
```

### Cards

- To activate this feature; [metadata](https://blacksmithgu.github.io/obsidian-dataview/annotation/add-metadata/) `cssclass` must have the value `cards` for that file

### Classdef

- Here, I had defined some custom css classes that I might require often. 
- You may also define your custom css classes here. Currently I have defined only for alignments.

Instead of `<p style=text-align:center>Text</p>` I can use the class `center` as follows:

```
<p class=center>Text</p>
```

### Color-Block

````
```note-gray-background
This is a Gray colour color block
```

```note-gray
This is a Gray text color block
```
````

- The above code snippets will generate the below Color Blocks

![[Color Block.png]]

### Image

```
![[bank.svg|grid|200]]![[Venn Diagram 3.svg|grid|200]]![[Shaykh Nurjan Mirahmadi.png|grid|200]] 
```

![[IMG Grids]]

---

```
 ![[Venn Diagram 3.svg|left|200]]
 # Lorem Ipsum
 **Lorem Ipsum** is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
 <i class="figcaption" id="left" style="width:200px">Test Image</i>
 **Lorem Ipsum** is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. 

```

![[IMG LCL + Text]]

---

```
![left|200](https://www.nurmuhammad.com/wp-content/uploads/cropped-Mawlana-Shaykh-Nurjan-Mirahmadi-2016.jpg)  *False Darkens the Heart and Truth Nourishes the Heart.*
<br>
==May It Be Blessed==
<i class="figcaption" id="left" style="width:200px">Test Image</i>
<br>
 **Lorem Ipsum** is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
```

![[IMG URL + Text]]
