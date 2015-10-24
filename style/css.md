# Opsee CSS Style Guide
## Table of Contents
  1. [CSS](#css)
    - [Formatting](#formatting)
    - [Classes Only](#classes-only)
    - [Ordering](#ordering-of-property-declarations)

### Formatting

* Use soft tabs (2 spaces) for indentation
* Always use camelCasing in class names. This lines up with our underlying tech (js) better.
* Put a space before the opening brace `{` in rule declarations
* In properties, put a space after, but not before, the `:` character.
* Put closing braces `}` of rule declarations on a new line
* Put blank lines between rule declarations

**Bad**

```css
/*good*/
.avatar {
  border-radius: 50%;
  border: 2px solid white;
}

/*bad*/
.avatar{
    border-radius:50%;
    border:2px solid white; }
.no, .nope, .not_good {
    // ...
}
#lol-no {
  // ...
}
```

### Classes Only
- Only use **single class** or element (if you have to) selectors.
    ```css
    /*good*/
    .foo {
        ...
    }
    body {
        ...
    }
    
    /*bad*/
    .foo .bar {
        ...
    }
    .foo > p {
        ....
    }
    ```
### Ordering of property declarations

1. `composes` declarations

    Just as in other OOP languages, it's helpful to know right away that this “class” composes another.

    ```css
    .btnGreen {
      composes btn;
      // ...
    }
    ```

2. Property declarations

    Now list all standard property declarations, anything that isn't `composes`.

    ```css
    .btnGreen{
      composes: btn;
      background: green;
      font-weight: bold;
      // ...
    }
    ```