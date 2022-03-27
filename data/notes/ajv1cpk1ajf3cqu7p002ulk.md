
## Headers

---

`# Header 1`

# Header 1 <!-- {docsify-ignore} -->

`## Header 2`

## Header 2 <!-- {docsify-ignore} -->

`### Header 3`

### Header 3 <!-- {docsify-ignore} -->

`#### Header 4`

#### Hheader 4 <!-- {docsify-ignore} -->

`##### Header 5`

##### Header 5 <!-- {docsify-ignore} -->

`###### Header 6`

###### Header 6 <!-- {docsify-ignore} -->

## Emphasis

---

`**This is bold text**`<br>
**This is bold text**

`__This is bold text__`<br>
**This is bold text**

`*This is italic text*`<br>
_This is italic text_

`_This is italic text_`<br>
_This is italic text_

`***This is bold and italic text***`<br>
**_This is bold and italic text_**

`___This is bold and italic text___`<br>
**_This is bold and italic text_**

`~~Strikethrough~~`<br>
~~Strikethrough~~

## Syntax highlight

---

### HTML

```html
<ul>
  <li>Google <a href="https://www.google.com">Site</a></li>
  <li>Microsoft <a href="https://www.microsoft.com">Site</a></li>
  <li>Apple <a href="https://www.apple.com">Site</a></li>
</ul>
```

### JavaScript

```javascript
setTheme = function (title) {
  var themes = document.querySelectorAll('[data-type="theme"]');
  themes.forEach(function (theme) {
    theme.disabled = theme.title !== title;
  });
};
```

### Typescript

```typescript
const language = "typescript";
```

### CSS

```css
.class {
  background: #808080;
}
```

### Java

```java
public static void main(String[] args) {
  System.out.println("Hello World!");
}
```

### SQL

```sql
SELECT object_name FROM dm_document WHERE r_modify_date >= DATE(TODAY);
```

### Inline Code

Value of `title` is empty.

---

## Tables

There must be at least 3 dashes separating each header cell.
The outer pipes (`|`) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

```markdown
| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| _Still_  | `renders` | **nicely** |
| 1        | 2         | 3          |
```

| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| _Still_  | `renders` | **nicely** |
| 1        | 2         | 3          |

Colons `:` can be used to align columns.

```markdown
| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |
```

| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |

---

## Horizontal Rule

Three or more...

Hyphens

`---`

---

Asterisks

`***`

---

Underscores

`___`

---

## Lists

---

### Unordered

```markdown
- Create a list by starting a line with `+`, `-`, or `*`
- Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    - Ac tristique libero volutpat at
    * Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
- Very easy!
```

- Create a list by starting a line with `+`, `-`, or `*`
- Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    - Ac tristique libero volutpat at
    * Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
- Very easy!

### Ordered

```markdown
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
```

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

```markdown
1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`
```

1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`

### Numbering offset

```markdown
57. foo
1. bar
```

57. foo
1. bar

### Mixed

```markdown
1. Ordered with `1.`
2. Ordered with `2.`
3. Ordered with `1.`
   - unordered with `-`
   * unordered with `*`
   - unordered with `+`
```

1. Ordered with `1.`
2. Ordered with `2.`
3. Ordered with `1.`
   - unordered with `-`
   * unordered with `*`
   - unordered with `+`

### Start list with number

```markdown
- 1968\. A great year!
- I think 1969 was second best.
```

- 1968\. A great year!
- I think 1969 was second best.

## Blockquote

---

```markdown
> Blockquote to the max
```

> Blockquote to the max

### Multiline

```markdown
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

### Big line

```markdown
> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can _put_ **Markdown** into a blockquote.
```

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can _put_ **Markdown** into a blockquote.

### Nested Blockquotes

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

## Links

---

```markdown
Go to [Google](https://www.google.com) and enjoy.
```

Go to [Google](https://www.google.com) and enjoy.

### Link to header

```markdown
Got to top header [Syntax Highlight](#syntax-highlight)
```

Got to top header [Syntax Highlight](#syntax-highlight)

## Images

---

```markdown
![Books](./assets/images/kb-logo.png)
```

![Books](./assets/images/kb-logo.png)

## Youtube Video

---

[![Youtube Video](https://img.youtube.com/vi/HUBNt18RFbo/0.jpg)](https://www.youtube.com/watch?v=HUBNt18RFbo)

## Reference

---

- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
- [ngx-markdown](https://jfcere.github.io/ngx-markdown/get-started)
- [Prism JS](https://prismjs.com/)

### Tags

`#markdown`
