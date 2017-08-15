---
layout: post
title: Z-Editor
description: A brief inroduction to Z-Editor
author: Nadun Indunil
header-img: assets/images/z.jpg
---

<br>

**Z notation** is a formal specification language used for describing and modelling computing systems. It is targeted at the clear specification of computer programs and computer-based systems in general. Z is based on the standard mathematical notation used in axiomatic set theory, lambda calculus, and first-order predicate logic. 

During the time I was learning Formal Methods of Software Engineering a major difficulty was to preparing the Z notation document. There was an editor tool named as Z tools for MS office but that didn’t support for OSX or Ubuntu operating systems.

![z-editor-gif](https://github.com/Z-Editor/Z-Editor/blob/master/gif/demo.gif?raw=true)

**[Z-Editor](https://z-editor.github.io/)** is an online editor that you can use to prepare your formal method documents without installing any plugins or IDEs. It is just a simple react application combined with awesome [draft.js](https://draftjs.org/) library. Still I have lot to implement but main functionalities such as printing the document is already implemented.


Left side toolbar of Z-Editor is provided with schema types

and

right side toolbar provides,
- Logics
- Sets
- Relations
- Functions 
- Sequences 
- Bags

notations.

folder structure of the project is as follows,

```
Z-Editor
│   README.md
│      
└───src
│   │  App.js
│   │  index.js 
│   │  ...
│   │
│   └───editor
│   │   │   config.js ---> contains configurations of toolbar
│   │   │   editor.js ---> main editor component
│   │   │   
│   │   └───schemas ---> basic schema components
│   │   │       Schemata.js
│   │   │       SchemataDown.js
│   │   │       SchemataUp.js
│   │   │
│   │   └───toolBar ---> toolbar components
│   │   │       sideToolBar.js
│   │   │       SideToolBarBtn.js 
│   │   │
│   │   └───edited-rdw
│   │   
│   │
│   └───images ---> basic schema btn images
│   
└───public
    │   index.html
```

In Z-Editor, schemas look like nested blocks but draft.js doesn’t support nested blocks (yet). The alternative was to create the schemas in plane blocks. Iconic schema tables were created using controlled css boundaries in between divs `<div>`. As an example main iconic schema is designed using upper bounded block, bar block, lower bounded block, bar block and lower bounded block respectively and the rest was handled by the awesome custom block rendering in the draft.js.

Each and every schema is a collection of:
- bar block
- upper bounded block  and 
- lower bounded block

<br>
Adding symbols was an easy part to do. When you click a button in the symbols toolbar that modifies the *contentState* and inserts the relevent symbol (config.js file stores the configurations and symbols for each and every button in toolbar). Then it pushes the *contentState* to *EditorState*.

Rich-Text-Utils Toolbar is extracted from [react-draft-wysiwyg](https://github.com/jpuri/react-draft-wysiwyg) and we are using an edited version. 

**important** : Z-Editor is only for editing and creating Z-notation documents, compiling your Z is not the objective of Z-Editor.

You can find the Github repo [here](https://github.com/Z-Editor/Z-Editor) and new ideas or improvements are welcome !  

