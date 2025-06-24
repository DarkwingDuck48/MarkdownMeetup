---
# try also 'default' to start simple
theme: seriph

background: https://cover.sli.dev
class: 'text-center'
# some information about the slides, markdown enabled
info: Начальный слайд
transition: slide-left
title: Markdown
fonts:
  sans: Fira Code
  serif: Fira Code
  mono: Fira Code
mdc: true
---

# Markdown

<div class="pt-12">
Как я перестал использовать Word
</div>
<div class="pt-12">
<span> Максим Бритвин </span>
</div>
<div>
<span> 25.06.2025</span>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# О чем поговорим?

1. Что такое Markdown и области его применения
2. Базовые возможности
3. Крутые фичи
4. Где мы сами можем его применять?


---
transition: fade-out
---

# История Markdown

<br>

Markdown - это язык разметки, **придуманный в 2004 году**.

- 📝 **Простота** - Синтаксис продумывался так, чтобы было просто изучать
- 🧑‍💻 **Удобство пользователей** - Понятный при чтении синтаксис
- 🛠 **Обрабатываемый** - Возможность обработать код компьютером

<br>
<br>

<!--
You can have `style` tags in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
layout: default
---

# Области применения

- Системы баг \ таск – треккинга. Jira, Readmine, GitHub Issues, GitLab ...
- Системы создания заметок и базы знаний. Notion, Obsidian,  Confuelnce, Wiki ...
- Мессенджеры.
- Документация при разработке 💡

---
transition: slide-down
---

# Какие инструменты нужны для редактирования?

| **Задача** | **Инструмент** |
| ------ | ---------- |
| Просто поправить файл| Любой текстовый редактор, даже Блокнот|
| Нужно посмотреть Preview файла | VS Code, Obsidian, Notepad ++ ... |


---
transition: slide-up
title: Основы синтаксиса - Заголовки
---

# Основы синтаксиса
<br>
Весь базовый синтаксис Markdown построен на простых тэгах. "#" Для определения уровня заголовка
<br>
<br>

# Заголовок 1 | \# Заголовок 1
## Заголовок 2 | \#\# Заголовок 2
### Заголовок 3 | \#\#\# Заголовок 3
#### Заголовок 4 | \#\#\#\# Заголовок 4
##### Заголовок 5 | \#\#\#\#\# Заголовок 5
###### Заголовок 6 | \#\#\#\#\#\# Заголовок 6

---
layout: image-right
image: https://cover.sli.dev
title: Основы синтаксиса - Строки
---

# Основы синтаксиса

Форматирование текста тоже максимально простое.

|Markdown| Синтаксис|
| -------| ---------|
|**Жирный** | \*\*Жирный\*\*|
|*Курсив* | \*Курсив\*|
|~~Перечеркнутый~~ | \~\~Перечеркнутый\~\~|


---
title: Основы синтаксиса - Списки
---

# Основы синтаксиса

Так же можно создавать списки.

<div grid="~ cols-2 gap-4">
<div>

Обычные списки:
- Элемент 1
  - Под элемент 1
- Элемент 2
  - Под элемент 2
    - Под элемент 3

</div>
<div>

Списки с нумерацией:
1. Элемент 1
   1. Под элемент1
2. Элемент 2
   1. Под элемент 2
      1. Под Элемент 3
</div>
</div>


---
class: px-10
transition: slide-up
---

# Крутые фичи, которые уже стали стандартом

Изначально был реализован только базовый функционал. Однако, сейчас уже есть несколько дополнительных тэгов, которые стали стандартом при создании документов.

<div grid="~ cols-2 gap-2" m="t-2">

Блоки кода с подсветкой синтаксиса

Как заработать на худи КОРУС:

```python
def sayHello(name: str) -> str:
  print(f"Hello, {name}!")
sayHello("Markdown")
```

- [ ]  Придумай тему митапа 💡
- [ ]  Сделай презентацию 😎
- [ ]  Расскажи коллегам 🎙
- [ ]  Получи монетки 👛

</div>

---
transition: slide-up
---

# LaTeX - Markdown для науки

Markdown стал очень популярен в научном сообществе - с помощью него, можно красиво оформить научные выкладки.

<br>

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$ {1|3|all}
\begin{array}{c}

\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} &
= \frac{4\pi}{c}\vec{\mathbf{j}}    \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array}
$$

<br>

---
transition: slide-down
layout: fact
---

# Диаграммы в Markdown


---
transition: slide-down
---

# Doc As Code
Подход к созданию и управлению документацией, при котором используются те же инструменты и практики, что и в разработке программного обеспечения.

1. Хранение документации в системе контроля версий (Git, GitLab)
2. Автоматизированная сборка и публикация
3. Коллаборация через Pull Request'ы и Code Review
4. Версионирование и управление изменениями

--- 
transition: slide-left
---

# Преимущества подхода

<br>

✅ Скорость и гибкость – быстрые правки, легкое обновление.

✅ Прозрачность – вся история изменений в Git.

✅ Автоматизация – меньше ручной работы при публикации.

✅ Проверка оформления на этапе публикации - можем ввести собственные стандарты оформления и строго им следовать. 

✅ Совместная работа – разработчики и технические писатели работают в одном workflow


---
transition: slide-right
layout: fact
---

# Покажу на простом примере

---
transition: fade
layout: center
---

# 🚫 No Office Used!

<br>

Ни один продукт Microsoft Office не был использован при подготовке к митапу!

--- 
transition: slide-up
---

# Полезные ссылки

<br>

🤩[Описание стандарта от разработчика Markdown - John Gruber](https://daringfireball.net/projects/markdown/)

👨‍💻 [GitHub для митапа](https://github.com/DarkwingDuck48/MarkdownMeetup#)

🗒️ [Cheat Sheet Markdown](https://www.markdownguide.org/cheat-sheet/)

🔥 [Презентации в Markdown](https://sli.dev)

📊 [Диаграммы в Markdown](https://mermaid.js.org/syntax/gitgraph.html)

📗 [Obsidian](https://obsidian.md/)
