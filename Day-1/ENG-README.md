## **Day 1: What is SCSS and Why Use It?**

**What is SCSS?**  
SCSS is like a more advanced version of CSS. In CSS, you often need to repeat the same code. For example:

```css
body {
  font-size: 16px;
  color: black;
}

.header {
  font-size: 16px;
  color: black;
}
```

You have to write the same color and font size everywhere. SCSS makes these things much easier. For instance:

```scss
$color: black;
$font-size: 16px;

body {
  font-size: $font-size;
  color: $color;
}

.header {
  font-size: $font-size;
  color: $color;
}
```

If you ever want to change the color, you only need to update the `$color` variable, and all your code will automatically use the new color.

**Why Use SCSS?**

**Convenience:** Manage colors and font sizes with variables.  
**Organization:** Keep your code neatly structured.  
**Efficiency:** Avoid repeating the same code.  
**Modularity:** Break your code into smaller, reusable parts.

**How to Use SCSS?**

1. **You’ll need a program to run SCSS on your computer.**  
   - Download and install Node.js.  
2. **Install Node.js.**  
3. **Then open the command line and run:**

```bash
npm install -g sass
```

4. **Create a `.scss` file.** For example:

```scss
$color: blue;

body {
  background-color: $color;
}
```

5. **Run SCSS and convert it into a CSS file:**

```bash
sass input.scss output.css
```

6. **Now you can use `output.css` in your browser!**

**What Else Can SCSS Do?**

**Nesting:** Place code inside other code.

```scss
.header {
  h1 {
    color: blue;
  }
}
```

This code becomes `.header h1 { color: blue; }`.

**Mixins:** Save commonly used code snippets and reuse them wherever needed.

```scss
@mixin centered {
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  @include centered;
  height: 100px;
  width: 100px;
  background-color: red;
}
```

**Math:** Mix colors or adjust sizes by multiplying or adding values.

```scss
$base-color: #333;
$secondary-color: lighten($base-color, 20%);
```

SCSS makes writing CSS more organized and fun. All you need to do is write a SCSS file, compile it into a CSS file, and enjoy easier, cleaner, and more scalable code. 😊
