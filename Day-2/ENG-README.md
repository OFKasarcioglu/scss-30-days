## **Day 2: What are SCSS Variables and How to Use Them?**

**Goals:**  
1. **Understand the concept of variables**  
2. **Learn how to define variables in SCSS**  
3. **Make writing code easier with variables**  

---

**📌 What are Variables?**  
Variables in SCSS allow you to define repetitive values once and use them throughout your code. This is especially helpful for colors, font sizes, and dimensions that you use frequently.

---

**📌 Defining Variables:**  
Variables are defined using the `$` symbol:  
```scss
$primary-color: #3498db;  
$font-size: 16px;  
$margin: 10px;
```

Now, you can use these variables anywhere:  
```scss
body {
  color: $primary-color;
  font-size: $font-size;
  margin: $margin;
}
```

If you ever change `$primary-color`, just update the variable and all your code will automatically use the new color.

---

**📌 Why Use Variables?** 

1. **Simplified Code Management:** If your project uses a primary color, a highlight color, and a few font sizes, you can define all these values as variables.  
2. **Reduced Error Risk:** Instead of writing color codes repeatedly, using a variable ensures you won’t make a mistake.  
3. **Easier Updates:** If you need to change your color palette, you only need to update the variables.

---

**📌 Example Color Palette:**  
```scss
// Color variables
$primary-color: #3498db;  
$highlight-color: #e74c3c;  
$background-color: #ecf0f1;

// Font sizes
$primary-font-size: 16px;  
$title-font-size: 24px;

// Margins
$primary-margin: 10px;
```

You can use these variables wherever needed:  
```scss
h1 {
  color: $highlight-color;
  font-size: $title-font-size;
}

p {
  color: $primary-color;
  margin-bottom: $primary-margin;
}
```

---

**Homework:**  
1. **Create a Color Palette:**  
   - Define three variables for primary color, highlight color, and background color.  
2. **Define Font Sizes:**  
   - Set different font sizes for body text and headings.  
3. **Apply Styles:**  
   - Use these variables to create basic styles for `h1`, `h2`, and `p` elements.  

---

