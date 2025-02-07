## **Day 3: What are Nested Rules and How to Use Them?**

**Goals:**  
1. Learn what nested rules are in SCSS  
2. Use nested rules to make code more organized  
3. Reduce repetition and create cleaner code

---

**📌 What are Nested Rules?**  
In CSS, a selector cannot be placed inside another selector. You have to write everything from scratch. For example:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header p {
  font-size: 16px;
}
```

In such cases, we constantly need to repeat the `.header` selector. In SCSS, we can simplify this structure by using nested rules.

---

**📌 Using Nested Rules in SCSS:**  
Nested rules in SCSS are written like this:

```scss
.header {
  background-color: blue;

  h1 {
    color: white;
  }

  p {
    font-size: 16px;
  }
}
```

When this code is compiled, it becomes:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header p {
  font-size: 16px;
}
```

**Why is it better?**  
- **Cleaner appearance:** No need to repeat `.header` selector every time.  
- **More organized:** Nested rules help you immediately understand which elements belong to which container.

---

**📌 Combining Selectors and Nesting:**  
In SCSS, you can not only nest element selectors but also combine other selectors:

```scss
.header {
  background-color: blue;

  h1 {
    color: white;

    &:hover {
      color: gray;
    }
  }

  .button {
    background-color: red;

    &:active {
      background-color: darkred;
    }
  }
}
```

This compiles to:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header h1:hover {
  color: gray;
}
.header .button {
  background-color: red;
}
.header .button:active {
  background-color: darkred;
}
```

---

**📌 Tips for Using Nested Rules:**  
- **Don’t overdo it:** Keep nesting levels shallow. If you nest too deeply, your code can become hard to read and manage.  
- **Use containers wisely:** Only use nested rules if the structure really calls for it.  
- **Quick editing:** When you need to make a change, all related styles are in one place.

---

**Homework:**  
1. Define a `.navbar` class.  
   - Add a `background-color`.  
   - Add a hover color for `a` elements.  
2. Define a `.sidebar` class.  
   - Nest styles for `ul` and `li`.  
3. Use these nested rules to make the code both organized and easy to read.

---

Using nested rules in SCSS helps us maintain cleaner, more organized code. **Let’s try these adjustments!** 🚀
