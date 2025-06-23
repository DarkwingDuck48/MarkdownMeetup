# 1. Главные команды Markdown

## 1.1. Базовые команды форматирования

### 1.1.1. Уровни заголовков

<center>

<!-- markdownlint-disable MD025 -->
# Heading 1 <!-- omit from toc -->
<!-- markdownlint-enable MD025 -->
## Heading 2<!-- omit from toc -->

### Heading 3<!-- omit from toc -->

#### Heading 4<!-- omit from toc -->

##### Heading 5<!-- omit from toc -->

###### Heading 6<!-- omit from toc -->

</center>

### 1.1.2. Начертания шрифтов
<!-- markdownlint-disable MD036 -->
**Жирный шрифт**

*Курсив*
<!-- markdownlint-enable MD036 -->
> Цитата

<u>Подчеркнутый</u>

~~Зачеркнутый~~

### 1.1.3. Списки

Что покажем из списков:

- Простой список
- Пошаговый
- Список с чекбоксами

---

**Как положить слона в холодильник?**

1. Взять слона
2. Открыть дверь
3. Положить слона в холодильник

---

**Как положить жирафа в холодильник?**

- [x] Открыть холодильник
- [x] Вытащить слона
- [ ] Положить жирафа

### 1.1.4. Особенные блоки

Просто одна строка кода
`print('hello')`

```python
# Если хотим подсветку синтаксиса конкретного языка, то можно использовать такой вариант

some_msg = "I love Markdown!"
print(some_msg)
```

Ссылки тоже можно 👍

[Ссылка гайд](https://www.markdownguide.org/cheat-sheet/)

[Ссылка на списки](#113-списки)

Можно вставить изображение - в полный размер изображения.
![alt text](images/pronyra.jpg)

Или изменить его так, как нужно.
<center>
<img src="images/pronyra.jpg" alt="drawing" width="200" style="transform:rotate(45deg);"/>
</center>

---

## 1.2. Таблицы

| Заголовок1 | Заголовок2 | Заголовок3|
|:-----------|------------:|:-----------:|
| 1|2|3|
|Привет<---| --->Мир| Очень большая строка, которую надо обязательно поместить! |

---

## 1.3. Сноски

В некоторых редакторах Markdown есть поддержка синтаксиса сносок [^1]

[^1]: Или сразу встроенная, или в качестве расширения

## 1.4. Схемы (Дополнительные обработчики)

Остальные примеры [тут](https://mermaid.js.org/ecosystem/tutorials.html)

```mermaid
gantt
    dateFormat  YYYY-DD-MM
    title       Диаграмма Ганта
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2025-06-01,2025-08-01
    Active task               :active,  des2, 2025-09-01, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2025-06-01,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :until isadded
    Functionality added                 :milestone, isadded, 2025-25-01, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```
