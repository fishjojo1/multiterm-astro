---
title: "Showing Off Blog Features"
published: 2025-07-20
draft: false
tags: ['astro']
coverImage:
    src: "./cover.jpg"
    alt: "A person with short, thick hair and prescription glasses sits at an organized workstation, using a magnification app to navigate a webpage. Their posture is proper and relaxed. On the desk: a computer, a mouse, a large desk lamp and a small notebook."
---

Since the post does not have a description in the frontmatter, the first paragraph is used.

## Theming

> Use your favorite editor theme for your blog!

Theming for the website comes from builtin Shiki themes found in Expressive Code. You can view them [here](https://expressive-code.com/guides/themes/#available-themes). A website can have one or more themes, defined in `src/site.config.ts`. There are three theming modes to choose from:

1. `single`: Choose a single theme for the website. Simple.
2. `light-dark-auto`: Choose two themes for the website to use for light and dark mode. The header will include a button for toggling between light/dark/auto. For example, you could choose `github-dark` and `github-light` with a default of `"auto"` and the user's experience will match their operating system theme straight away.
3. `select`: Choose two or more themes for the website and include a button in the header to change between any of these themes. You could include as many Shiki themes from Expressive Code as you like. Allow users to find their favorite theme!

> When the user changes the theme, their preference is stored in `localStorage` to persist across page navigation.

## Code Blocks

Let's look at some code block styles:

```python
def hello_world():
    print("Hello, world!")

hello_world()
```

```python title="hello.py"
def hello_world():
    print("Hello, world!")

hello_world()
```

```shell
python hello.py
```

Also some inline code: `1 + 2 = 3`. Or maybe even `(= (+ 1 2) 3)`. 

See the [Expressive Code Docs](https://expressive-code.com/key-features/syntax-highlighting/) for more information on available features like wrapping text, line highlighting, diffs, etc.

## Basic Markdown Elements
- List item 1
- List item 2

**Bold text**

*Italic text*

~~Strikethrough text~~

[Link](https://www.example.com)

> In life, as in art, some endings are bittersweet. Especially when it comes to love. Sometimes fate throws two lovers together only to rip them apart. Sometimes the hero finally makes the right choice but the timing is all wrong. And, as they say, timing is everything.
>
>\- Gossip Girl

| Name      | Age | City         |
|-----------|-----|--------------|
| Alice     | 30  | New York     |
| Bob       | 25  | Los Angeles  |
| Charlie   | 35  | Chicago      |

___

## Images

Images can include a title string after the URL to render as a `<figure>` with a `<figcaption>`.

![Pixel art of a tree](./PixelatedGreenTreeSide.png "Pixel art renders poorly without proper CSS")

```md title="Pixel art markdown" wrap
![Pixel art of a tree](./PixelatedGreenTreeSide.png "Pixel art renders poorly without proper CSS")
```

I've also added a special tag for pixel art that adds the correct CSS to render properly. Just add `#pixelated` to the very end of the alt string.

![Pixel art of a tree #pixelated](./PixelatedGreenTreeSide.png "But adding #pixelated to the end of the alt string fixes this")

```md title="Pixel art markdown with #pixelated" wrap
![Pixel art of a tree #pixelated](./PixelatedGreenTreeSide.png "But adding #pixelated to the end of the alt string fixes this")
```

## Admonitions

```md title="Admonition example in markdown"
:::note
testing123
:::
```

:::note
testing123
:::

:::tip
testing123
:::

:::important
testing123
:::

:::caution
testing123
:::

:::warning
testing123
:::

## HTML Elements

<button>A Button</button>

### Fieldset with Inputs

<fieldset>
    <input type="text" placeholder="Type something"><br>
    <input type="number" placeholder="Insert number"><br>
    <input type="text" value="Input value"><br>
    <select>
        <option value="1">Option 1</option>
        <option value="2">Option 2</option>
        <option value="3">Option 3</option>
    </select><br>
    <textarea placeholder="Insert a comment..."></textarea><br>
    <label><input type="checkbox"> I understand<br></label>
    <button type="submi">Submit</button>
</fieldset>

### Form with Labels

<form>
<label>
    <input type="radio" name="fruit" value="apple">
    Apple
</label><br>

<label>
    <input type="radio" name="fruit" value="banana">
    Banana
</label><br>

<label>
    <input type="radio" name="fruit" value="orange">
    Orange
</label><br>

<label>
    <input type="radio" name="fruit" value="grape">
    Grape
</label><br>

<label>
    <input type="checkbox" name="terms" value="agree">
    I agree to the terms and conditions
</label><br>


## Latex math support
You can also display inline math $ \frac{a}{b} \cdot b = a $ like so `$ \frac{a}{b} \cdot b = a $ `



## Shortcode emoji support
Emojis can be displayed using shortcodes as well with remark-gemoji! 
<br>
:smile: `:smile:`
 