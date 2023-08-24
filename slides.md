---
layout: cover
highlighter: shiki
css: unocss
colorSchema: dark
transition: fade-out
growSize: 1.5
title: 了解一下 Web Accessibility
---

<img class="w-60 absolute top-10 left-10" src="/type-challenges-logo.svg" />

# 了解一下 Web Accessibility

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    立即前往 <carbon:arrow-right class="inline animate-fade-out-right animate-count-infinite animate-duration-1.5s"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit /> 
  </button>
</div>


---
transition: fade-out
layout: intro
growX: 10
growY: 90
style: 'padding-left: 8rem;'
---

# Web Accessibility (web A11y)

> Web Accessibility 是指任何人(这里的任何人，无论是健全人还是残疾人，无论是年轻人还是老年人等等)在任何情况下都能平等的、方便的、无障碍的获取信息和利用信息。

- 听觉障碍:使用视频时，确保它有完整的字幕。使用音频时，别忘了文本描述
- 视觉障碍:足够的对比度。支持读屏软件
- 运动障碍:同时对鼠标和键盘有很好的支持
- 认知障碍:避免快速的移动，晃动等效果。

---
layout: center
growX: 50
growY: 120
growSize: 1.5
---

# Web Accessibility Core

<!-- <div class="number-bg">1</div> -->
<WACore />

---
layout: center
growX: -10
growY: 50
growSize: 0.75
---

##  WCAG - Web Content Accessibility Guidelines
<br>

| Rule ID      | Rule Description                                                                                       |
|--------------|--------------------------------------------------------------------------------------------------------|
| [1.1.1 Non-text Content](https://www.w3.org/TR/WCAG22/#non-text-content)        | Provide text alternatives for non-text content that serves the same purpose.         |

<br>

``` html
<!-- Example -->
<img src="./img.png" ale="">
```

---
layout: center
growX: 100
growY: 80
growSize: 1.5
---

### WCAG 的四个原则

- [Perceivable](https://www.w3.org/TR/WCAG22/#perceivable) (感知性) - 信息和用户界面组件必须对用户可感知
- [Operable](https://www.w3.org/TR/WCAG22/#operable) (可操作性) - 用户界面组件和导航必须是可操作的
- [Understandable](https://www.w3.org/TR/WCAG22/#understandable) (理解性) - 信息和操作用户界面必须是理解的
- [Robust](https://www.w3.org/TR/WCAG22/#robust) (健壮性) - 内容必须是健壮的，可靠的，以及与当前和未来的用户代理兼容的


---
layout: center
growX: -10
growY: -10
class: text-center
---

### WCAG 的三个级别

<br>

- A级 (最低)
- AA级 (中等)
- AAA级 (最高)

--- 

### WCAG Guidelines

<br>

- [w3.org/TR/WCAG22/](https://www.w3.org/TR/WCAG22/)
- [wcag-checklist](https://www.wuhcag.com/wcag-checklist/)
- [checklist](https://webaim.org/standards/wcag/checklist)

---
layout: center
growX: 50
growY: 0
---

### ARIA - Accessible Rich Internet Applications

<div  grid="~ cols-1 gap-4" mt-6>
<div v-click>

#### Html with ARIA

```html
<nav aria-label="router">
  <ol id="menubar" role="menubar" aria-label="router">
    <li role="none">
      <a href="#" role="menuitem" aria-haspopup="true" aria-expanded="false">
        Home
      </a>
    </li>
    <li role="none">
      <a href="#" role="menuitem" aria-haspopup="true" aria-expanded="false">
        Library
      </a>
    </li>
    <li role="none">
      <a href="#" role="menuitem" aria-haspopup="true" aria-expanded="false">
        Data
      </a>
    </li>
  </ol>
</nav>
```

</div>
<div v-click>

#### Screen Reader

* router navigation landmark
* router submenu 1 of 3 

</div>
</div>

---
layout: center
growX: 50
growY: -50
growSize: 1.5
---

### ARIA Roles and Attributes
* [Roles](https://www.w3.org/TR/wai-aria-1.2/#roles_categorization)
   * [Widget Roles](https://www.w3.org/TR/wai-aria-1.2/#widget_roles)
   * [Document Structure Roles](https://www.w3.org/TR/wai-aria-1.2/#document_structure_roles)
   * [Landmark Roles](https://www.w3.org/TR/wai-aria-1.2/#landmark_roles)

* [Attributes: State and Property](https://www.w3.org/TR/wai-aria-1.2/#state_prop_taxonomy)
  * [Widget Attributes](https://www.w3.org/TR/wai-aria-1.2/#attrs_widgets)
  * [Live Region Attributes](https://www.w3.org/TR/wai-aria-1.2/#attrs_liveregions)
  * [Drag-and-Drop Attributes](https://www.w3.org/TR/wai-aria-1.2/#attrs_dragdrop)
  * [Relationship Attributes](https://www.w3.org/TR/wai-aria-1.2/#attrs_relationships)


---
transition: fade-out
layout: center
growX: 10
growY: 90
style: 'padding-left: 8rem;'
---

#### ARIA - Landmark Roles

<div  grid="~ cols-2 gap-4" mt-6>
<div v-click>

#### [Landmark Roles](https://www.w3.org/TR/wai-aria-1.2/#landmark_roles)
- [application](https://www.w3.org/TR/wai-aria-1.2/#application)
- [banner](https://www.w3.org/TR/wai-aria-1.2/#banner)
- [complementary](https://www.w3.org/TR/wai-aria-1.2/#complementary)
- [contentinfo](https://www.w3.org/TR/wai-aria-1.2/#contentinfo)
- [form](https://www.w3.org/TR/wai-aria-1.2/#form)
- [main](https://www.w3.org/TR/wai-aria-1.2/#main)
- [navigation](https://www.w3.org/TR/wai-aria-1.2/#navigation)
- [search](https://www.w3.org/TR/wai-aria-1.2/#search)
  

</div>
<div v-click>

#### Screen Reader

<img src="/public/landmark.svg" />

</div>
</div>

<div v-click mt-10px>
* https://www.w3.org/WAI/ARIA/apg/patterns/landmarks/examples/general-principles.html
</div>

---
growX: 50
growY: 120
growSize: 1.5
---

### ARIA - Landmark

| HTML Element | Landmark Role |
| --- | --- |
| `<header>` | `banner` |
| `<nav>` | `navigation` |
| `<main>` | `main` |
| `<aside>` | `complementary` |
| `<footer>` | `contentinfo` |
| `<form>` | `form` |
| `<article>` | `article` |
| `<section>` | `region` |
| `<aside>` | `complementary` |
| `<div>` | `region` |

---
layout: center
---

### ARIA - Best Practices

- [ARIA Best Practices](https://www.w3.org/WAI/ARIA/apg/example-index/)


---
layout: center
growX: -30
growY: 50
growSize: 1.5
---

#### Headings
> Heading可以传递页面的层级结构，有利于用户了解页面结构

- 按等级嵌套标题。最重要的标题排名1 (`<h1>`) ，最不重要的标题排名6(`<h6>`)。
- 级别相等或更高的标题将启动一个新章节。
- 跳过标题列可能会造成混淆，应尽可能避免

---
layout: center
growX: 110
growY: -10
---

#### Page Title
> 提供唯一、简洁的页面标题有助于残疾用户快速理解网页的内容和用途

- 提供准确描述页面内容和用途的简明页面标题
- 确保页面标题对于您的站点和任何相关站点都是唯一的
- 首先放置页面描述文本，然后是站点名称
- 使用JavaScript更改标题，以适当地反映主内容动态更改的页面的页面内容(例如，单页应用程序)

---
layout: center
growX: 90
growY: 90
growSize: 1.5
---

## 使用工具

- [axe DevTools](https://www.deque.com/axe/devtools/)


### More
- 键盘的支持
- 正确的内容，指导用户，有意义的值，多语言

---
layout: intro
class: text-center pb-5
growX: 50
growY: 0
---

# Thank You!

Slides on 东方
