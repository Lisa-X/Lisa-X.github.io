---
layout: article
title: Ingredients for New Posts
tags: ingredient
key: 20200729
aside:
  toc: true
---
<!--more-->

# Source

Here are what you need to create a new post.

- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

- [Markdown Cheatsheet](https://wordpress.com/support/markdown-quick-reference/)

- [Cute Markdown Emoji:heart_eyes:](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

- [LaTeX / Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)

- [Formula Box](https://www.codecogs.com/latex/eqneditor.php)

Here is a check list of sources to be learned.
- [spec Markdown](https://spec-md.com/#)



# Problems & Solutions
## Change Logo
Replace the logo.svg file in `.\Lisa-X.github.io\_includes\svg` <br>

![logo_scn.png](https://github.com/Lisa-X/Lisa-X.github.io/raw/master/pics/screenshots/logo_scn.png)

## Change Favicon

# Cheatsheet
## Icons for Commit Message

- Test 试验性操作，瞎搞<br>
:no_mouth: `:no_mouth:` <br>
:pig: `:pig:`

- 搭建相关<br>
:house: `:house:`

- 美化相关<br>
:sparkling_heart: `:sparkling_heart:`<br>
:cherry_blossom: `:cherry_blossom:`

- Edit a new post<br>
:memo: `:memo:`<br>
:pencil2: `:pencil2:`

- Else 常用<br>
注意事项：:warning: `:warning:`<br>
照片：:camera: `:camera:` <br>
坐标：:round_pushpin: `:round_pushpin:` <br>
想法idea：:bulb: `:bulb:`\\
例题：:notebook: `:notebook:` 

## Math Formula Cheatsheet
- add space `$~$`
- add underbrace/overbrace\\
`$\underbrace{I_j (x) \ast \Delta_j(x,t_l,p)}_{I_j(x)(x-v_j(t,p))}dx$`\\
$\underbrace{I_j (x) \ast \Delta_j(x,t_l,p)}_{I_j(x)(x-v_j(t,p))}dx$
`$dr=\underbrace{a(b-r)}_{m(t)}dt +\underbrace{\sigma\sqrt{r}} _{n(t)}dz$`\\
$dr=\underbrace{a(b-r)}_{m(t)}dt +\underbrace{\sigma\sqrt{r}} _{n(t)}dz$
- font color\\
`$\color{color wanted}{colored text}$`\\
$\color{green}{The~font~color~should~be~green}$\\
$\color{blue}{The~font~color~should~be~blue}$

## Markdown Cheatsheet
- **bold** `**bold**`

- *intalic* `*italic*`

- ***bold&italic*** `***bold&italic***`

* bullet points: - / *

* code line: ` <br>
`a = b + c`

* code block (python): ```py <br>
```py
def sum(x):
    sum = 0
    for i in range(x+1):
        sum = sum + i
    return sum
```
```py    
print(sum(3))
> 6
```

- Blockquote: >
> Here is a quoted line <br>
> Another line

- Add image

<img src="https://i.loli.net/2020/07/30/FbfqkdXGzs3rWvo.jpg" width = "300" height = "300" alt="avatar" align=center />

```html
<img src="https://i.loli.net/2020/07/30/FbfqkdXGzs3rWvo.jpg" width = "300" height = "300" alt="avatar" align=center />
```

![avatar_temp.jpg](https://i.loli.net/2020/07/30/FbfqkdXGzs3rWvo.jpg){:width="200px" height="200px"}

```md
![avatar_temp.jpg](https://i.loli.net/2020/07/30/FbfqkdXGzs3rWvo.jpg){:width="200px" height="200px"}
```

- Template for a picture card.
<div class="card">
  <div class="card__image">
    <img class="image" src="https://github.com/Lisa-X/Lisa-X.github.io/raw/master/pics/avatar.jpg"/>
  </div>
  <div class="card__content">
    <div class="card__header">
      <h4>TRY PIC</h4>
    </div>
    <p>
      This is my avatar pic.
    </p>
  </div>
</div>


<!--more-->


---
