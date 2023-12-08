## Key Board Shortcuts

> - The following keyboard shortcuts listed are Obsidian Shortcuts that I Set Up
> - You can customize or view existing keyboard shortcuts: `Settings > Hotkeys`

Shortcut | Purpose
--|--
Alt + T | Insert a Template
Alt +  L | Toggle Bullet List
Alt +  N | Toggle Numbered List
Alt +  B | Toggle Blockquote
Alt + C | Toggle Callout
Alt + D | Delete Current File
Alt + H | Highlight Text
Ctrl + N | Create a New Note ➡️ Create a New Note in Current Tab

## Templates

> - Templates are placed on: `Maintenance/Templates`
> - When you copy and paste an image directly to the page 
> 	- It will create a folder Attachments within that folder and will place the image there

**Main**

```
---
created_date: {{date}}
created_time: {{time}}
alias: {{title}}
cssclass: 
page-no: 
note:
  aspect: 
  section: 
tags: 
---
```

<p align=center><img src=https://github.com/zak-admin/My-Obsidian-Vault/blob/main/Media/Main%20Template.png></p>

- This Template is the main template I use for every of my pages.
- When you insert this template. This will automatically fill created date, time and title for the page.
- In the metadata, you can change the alias, cssclass, page-no, note.aspect, note.section, tags.
- note.aspect can be regarded as Category and note.section as Sub Category
- These metadatas' will be hidden from reading view. They can be edited in editor mode.
- The `to-main` link acts as a default link for back to homepage.
- The `back-to` link can be edited with the link of previous page.
- The `id` can be a unique identifier for that page
- All these details are filled in order to make the index using dataview and for navigation.

**main dataview**

````
```dataview
TABLE WITHOUT ID page-no AS X, link(file.link, alias) AS NAME
WHERE back-to = this.file.link
SORT page-no
```
````

- This is the main dataview template used for index pages.
- This is a table query where it will show the
	- `page-no` under X column
	- `alias` as a file link under Name column
- Where the file metadata `back-to` is linked to current file which is the index file
- And will be sort by the `page-no`

**archive dataview**

````
```dataview
TABLE WITHOUT ID page-no AS X, link(file.link, alias) AS NAME
WHERE file.folder = this.file.folder AND file != this.file AND back-to != this.file.link OR flt-to = this.file.link
SORT page-no
```
````

- This is an additional dataview query in the index page.
- This will be after the main dataview template of the index page.
- This will display all the files that present within current folder but not linked to index
- This can also be as a form of listing other related notes but not part of a main,
- This is a table query where it will show the
	- `page-no` under X column
	- `alias` as a file link under Name column
- Where file in this folder and not this index file and `back-to` has no this file link or `flt-to` is this file
- That means to have an index of an archive note. You can alter that page metadata back to flt and link
- And will be sort by the `page-no`

**main education**

```
class:
  fee: 
  vendor: 
  tutor: 
```

- this is an altered version of main with some additional metadata for education.
- class.fee, class.vendor, class.type, class.tutor are the additional metadata.
- class.vendor can be youtube, udemy, coursera, an educational institute etc...
- this is just to keep track over the class or course details

## My Vault Structure

Folder | Purpose
--|--
Maintenance | This folder contains all Obsidian Maintenance Notes
Fleeting Notes | This folder contains frequent unorganized quick jot down notes
Literature Notes | These are notes you take according to a subject syllabus
Permanent Notes | These notes are generated when fleeting or literature turns out to be permanent
