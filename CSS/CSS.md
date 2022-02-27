Website - Color Hunt, DevDocs, Emojipedia(For Emoji), Codepen(for coding web in website)
## Inline, External CSS
- Without creating another css file we just inject css in the same html code but the problem is we have to modify each and every tag no matter there if functionality is same
- to apply css code across the whole web page we have to create a separate file for css

### Notes
- There are some default css code comes with the tags being applied by your browser and we override the default values of it by specifying our own values to it.
- pretty much everything that exist on the web page is nothing but boxes, *you can use a chrome plug in called pesticide to view all how the boxes are formatted*
- Suppose you specifying width of a html tag with some hard coded value and when your web page will be used in computer or mobile or ipad then it will definitely look odd so thats why we use percentage instead of the hard coded values
- Inline css has more precedence than external css, suppose you define body color at 2 places, one is at body tag that is inline code and another one is in css file that is external, then the color that is specified in body tag will reflect in the web site
- **background-color: blue**
- **height - changes the height of your box**
### Exercise
- How to modify the border style line
- Change the h1 and h3 header color
- How to debug the code
## Anatomy Of CSS
- Syntax means grammar of the programming 
```
body {
background-color : red;
}
```
- Here body is the selector part, it says what to select then the properties part and then its value
### Notes
- The class attribute allows us to differentiate all of our different HTML elements and it start with dot symbol
## Class vs ID
- class is more specific than id , mean if you change 1 element with class and id then the properties that are specified in the class will be reflect in the web page
- Use classes when you want to affect a group of elements and use id for affecting only one element because you can give only one to a specific element
- they are more specific than tag selector
- you can add more than one class to a html element but you cant have more than one id for a particular element
## Pseudo Class
### Exercise
- play with :hover  
## Favicon
## Div
- Div stands for content division element and it basically allows you to split up or divide your content into separate container or boxes so that you can affect the layout of each box separately
## The Box Model
### Note
- `borde-width : 0px 10px 20px 30px;` and it goes in a circular manner clock wise, means the first one is for top, second one is for right, third one is for bottom and last one is for left
## CSS Display Property
- The display property has four different values, (block, inline, inline-block, None)
### Notes
- Block elements are those which takes whole width of the display, and here block means blocking out all the elements from its left or right
- common block elements are paragraphs, heading, divisions, list and items and forms
- span elements are inline elements, in only takes that much of the size as its data inside it required
- you cant change the width of a span element 
- you can modify any elements display property but the problem is when you modify display properties of the inline elements to block then you cant modify its width and similarly when you modify the block elements display property to inline then you also cant modify its height, so here question arises how can we achieve both properties? so the answer is you can use another display property that is inline-block
- again if you use the none display property then it basically delete that element from the web page
- again if you use the property visibility: hidden then its just work same like none display but its occupies its size but does not show the element
## CSS Static vs Relative
## Absolute Positioning
## Centering Elements
## Goal
- The main motive of a web developer is How to do something that is specific to your own need 
- best practice to order all the properties in alphabetic order, it helps to debug when there are a lots of codes 