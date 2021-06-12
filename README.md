# Git repository to store css art

Current status: 👍 - 💻
<pre>
├── master
    ├── ...
    └── 1 - Simple shapes: using square, circles, transform & border
    └── 2 - Border radius & gradient: using border radius for overall shape, gradient for 3D effect and dimension
</pre>


## Intro - The Tools (CSS concepts)
### Box Model
As we know, everything in CSS is a box. So, a rectangle(or square) is the basic shape we will manipulate to create every other shape. This is the raw material.
By default, the size (width, height) of a box is determined by the content and specified margin, padding. As we won't be having any HTML content, we need to explicitly mention the width and height of the (block) boxes - div is the normally used element.

### ::before, ::after
Along with every element we also have the pseudo-elements ::before and ::after as two additional boxes at our disposal. We can use those for some details as an alternative to adding more elements in our markup. (A good usage is adding new elements for different parts, and using pseudo-elements to add details like shades, patterns to a part).

> Don't forget to add content:'' - without content, the pseudo-element won't be generated.  

### Positioning
A very important aspect of CSS art is positioning the shapes for alignment or for creating complex shapes from basic ones.
That requires manipulation of the co-ordinates of the shapes. To do that, we may need to set an absolute or relative positioning.

In a lot of case it helps to set *{position: absolute} - it's easier to calculate position relative to the parent element. But it's not always necessary - we can use relative positioning, or even flex/grid based on the particular use case (Flex with justify-content is a great tool for centering elements). The main point is figuring out how the different boxes are to be positioned with each other.

Along with positioning, z-index is handy to position elements in front of or behind other elements. *It helps to dig a bit into stacking context to deepen our understanding of z-index to wield it well.

### DOM structure
This doesn't actually affect the CSS art as such. It's more about good practice for maintainable stylesheets . It better to have a hierarchy of elements to create the parts that make up the whole drawing. Ex: eyes divs should be placed inside a head div, if possible using ::before, ::after of an element for creating details only of that element (this won't and needn't be true if you are constraining the number of elements)

### Border-radius
Now, we will move on to manipulating the square into different shapes.

Border-radius is a great way to create not only circles and ellipses, but also organic looking shapes.
Here is the tool to easily you can use to [generate radius](https://9elements.github.io/fancy-border-radius/).
And this [video](https://www.youtube.com/watch?v=j3Z4DR0o8bk) to understand the property and result, especially control around horizontal and vertical radius.
> border-radius: hborder / vborder  

### Box-Shadow
While creating CSS art, box-shadow can be used create copies of a shape in addition to simulating a 3d effect. Multiple box-shadows can be applied to an element to create multiple copies of different sizes. Inset borders can be used to create shadows as well.

### Clip Path
Clip-path is another way to create custom shapes.

The clip-path CSS property creates a clipping region that sets what part of an element should be shown.
Here is a tool to easily [generate clip path](https://bennettfeely.com/clippy/).
> Some shapes (ex: triangles, trapezoids) can be made using border as well as through clip-path. One advantage of clip-path over border is that it is easier to apply gradients.  
> border-radius and box-shadow may not play well with clip-path  

### Gradients
Gradient is one of the most common tool used in CSS art. In websites, gradients are used for smooth transitions between two or more specified colors. However, once we know how to, gradients can be used to create shapes, patterns, shading, etc. in CSS art.

Multiple gradients can be applied separated by commas, and remember backgrounds are rendered from bottom(last) to top(first). 
Here is an article to easily [understand css gradients](https://css-tricks.com/drawing-images-with-css-gradients/).

### Breaking down objects into basic shapes
Again, this is not exactly a CSS property, but an essential requirement for CSS art. We break down what we want to draw into basic shapes (boxes, circles, semicircles, triangles, trapezoid, etc.), and try to think how those shapes combine, overlap or aligned to create our design.
We will initially have some idea about how those shapes can be generated (new element, copy through box shadow, through border-radius, or through gradients).  


## 1 - Simple shapes
### Koala - 👍
> _https://codepen.io/FGAUTREAULT/pen/eYvZwoZ_  
![Simple shapes - Koala](assets/result-koala.png)

### Ice cream - 👍
> _https://codepen.io/FGAUTREAULT/pen/BaWzZEv_  
![Simple shapes - Ice cream](assets/result-icecream.png)

## 2 - Border radius & Gradient
### Lamp - 👍
> _https://codepen.io/FGAUTREAULT/pen/oNZadYP?editors=1100_   
![Border radius & Gradient - Lamp](assets/result-lamp.png)

## Resources for inspiration
> _https://codepen.io/poulamic/full/eYJWrNE_  
> _https://codepen.io/poulamic/pen/mdPPqbx_  
> _https://a.singlediv.com/_  
> _https://codepen.io/hylobates-lar/pen/WNwRjbQ_  
> _https://codepen.io/aitchiss/pen/eYpXodg_  
> _https://codepen.io/jkantner/pen/ELvMBE_  
