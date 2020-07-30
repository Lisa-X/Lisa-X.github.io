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

- [Cute Markdown Emoji:heart_eyes:](https://gist.github.com/rxaviers/7360908)

# Cheatsheet

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
