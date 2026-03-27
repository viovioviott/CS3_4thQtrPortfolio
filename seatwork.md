<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="Castillo, Sophia Violet C" />
  <meta name="revised" content="March 27, 2026" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

- The addition of the relative positioned changed the position relative to its default position. As you add different vales to top and left, the div will move towards those positions based on the values given.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

- As you scroll, the div stays in place. This addition allows the div to remain fixed relative to the viewport (visible screen), unlike ```position: relative; ``` where the movement is only relative to its default position.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

- ```Position: absolute``` allows the div to be relative to nearest positioned ancestor or initial containing block (usually the viewport). Unlike fixed and relative, the position is based on the nearest positioned ancestor and will only be relative to the vieport if no previous ancestor is present.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?

- The addition of z-index controls the stacking order of elements with the higher values at the front. As you change the z-index values of different elements, the greater value will remain at the front most position.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? 
      - To get the .notice box to be at that position, it has to be placed relative to .content box. This can be done using absolute and relative positions:

      ```html
      <div class="notice">Notice</div>
      ```


    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    b. How does absolute positioning depend on its parent element?

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
