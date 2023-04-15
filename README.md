# html-css-practise

Creating youtube mock

---
Nested Layout Technique:
Every Design can be broken into vertial and Horizontal Layout | The layouts are combination of these two
![Reference](/asset/learning/layouts.png)

Divs are block element by default and therefore they take up the entire line and appear one on top of other

<div></div>
<div></div>

Also, Divs by Default have width of 100 percent
In case we make the divs inline-block but we need to adjsut the width so that they appear inline

```
.channel-picture {
    display: inline-block;
    width: 50px;
    vertical-align: top;
}

.video-info {
    display: inline-block;
    width: 200px;
    /* vertical-align: top; */
}
```

Images by Default Overflow to keep there original dimensions thats what causes them to overflow
Resizing the image should be done to fit it and not to overflow
channel-picture has width of 50px so you can have equal to it or less then that
```
.profile-picture {
    width: 40px;
    border-radius: 50px;
}
```

The better way would be to give 100 percent to match the parent element width
```
.profile-picture {
    width: 100px;
    border-radius: 50px;
}
```

------------------------------------------------------------------------------------------------------------------------
Paragraph: p come with a default margin at top and bottom
How you can get rid of the margin 
```
.video-title {
    /* width: 300px */
    margin-top: 0
}
```

------------------------------------------------------------------------------------------------------------------------
What if you need to make the image round, rounded corners?
border-radius is the css property for it 
```
.profile-picture {
    width: 40px;
    border-radius: 50px;
}
```
------------------------------------------------------------------------------------------------------------------------
To add the margin on the bottom?
margin-bottom is the css property
```
.thumnail-row {
    margin-bottom: 12px
}
```
------------------------------------------------------------------------------------------------------------------------
This project is using the Google font called roboto
You can use the external font or css. To add this to your project you can add it to the headers

------------------------------------------------------------------------------------------------------------------------

This syntax with a comma is called a font stack. This is the Backup in case we donot have roboto font family then it will take Arial

Basically let us setup the backup font by any reason the roboto fail to load from google then Arial will be loaded
font-family: Roboto, Arial;

------------------------------------------------------------------------------------------------------------------------

Why we have this css Class?
line-height: 18px;
To change space between the lines 

------------------------------------------------------------------------------------------------------------------------

Have a look into the computed tab in the Developers tool

------------------------------------------------------------------------------------------------------------------------

To remove the defualt margin from the p elements top and bottom margin is kept to 0
p {
    font-family: Roboto, Arial;
    margin-top: 0;
    margin-bottom: 0;
}

------------------------------------------------------------------------------------------------------------------------
New Lesson : Css  Grid
This helps making the horizontal layout and also the grid like youtube pages much easier

Till now we are using display: inline-block and adding, adjusting the width to put the divs side by side 
There are some problems with display: inline-block

inline blocks have some alignment problems There are some spaces it takes that is adding the div to the next line

Second problem its not vertically alligned


New Technique is CSS GRID: THis give help us create perfectly aligned horzontal layouts

What is A Grid?
A grid is a layout that has Rows and Column
One Row two Column layout

![Grid with one by two layout](/asset/learning/grid-layout.png)

If the div is placed in the grid it takes the entire column instead

Grids makes the alignment much better and also doesnot take the space that inline-block takes
![Grid example](/asset/learning/grid-example.png)


If we have more elements then the columns we specify in the grid-template-columns: 100px 100px 200px, it starts to wrap around and create new rows
![Grid with extra row](/asset/learning/grid-with-extra-div.png)


grid-template-columns: 100px 1fr: fr: basically says to take the remaining space in the grid

One more feature of the grid system
grid-template-columns: 100px 1fr 2fr the free space work in the form of the ratio 

------------------------------------------------------------------------------------------------------------------------

Remember : Spacing Inside is called padding

------------------------------------------------------------------------------------------------------------------------

if we have extra divs in the grid it starts wrapping in the next row

------------------------------------------------------------------------------------------------------------------------

Flexbox:
Another way of creating the Layouts is using flexbox
Flexbox is similar to css grid(but its more flexible)

Flexbox is very flexible one and have a horizontal alignment 

flex: 1 is equivalent to 1fr in the grid system

Similar to the fr in the column we have flex in the flexbox


What is the difference between the grid and flex
The Grid is more rigid because first we need to define the columns and then we add the columns
But with the flexbox the flex  is been given to the divs, elements take there width along with them if they are moving
around and this helps in flexible layouts depending on how many elements we have and what order they are in.

That is the biggest different between the grid: rigid and flex box: flexible

What is the advantage of having the flexible layout
Where we need flexible layout depending on our content

justify-content: start: A property of flexbox if given the valid of start it will start from the left side
justify-content: end;
justify-content: center

Look it into all the different values

align-items: end
This is to align the divs or containers horizontally in the main container: values can be start end and center

------------------------------------------------------------------------------------------------------------------------

How is the Header Designed?
We see the left and right are having the same width if we are adjusting the screen size but as we are reducing the 
screen size we see the search Bar that is the center div is adjusting and becoming small

so we keep the left and right to fixed width and center to adjustable one
flex: 1 for adjusting the center tab

------------------------------------------------------------------------------------------------------------------------
box-shadow: what all property do we need to check those

------------------------------------------------------------------------------------------------------------------------

margin-left: -1: negative margin substracts the space and pulls the element to that side


flex-shrink: 0: this is the property of flex which doesnot allow the shrinking


----------------------------------------------------------------------------------------------------------------------

width: 0
Normally the input box has some width but to not have that width you can keep the width to 0


----------------------------------------------------------------------------------------------------------------------

css position: 

Why Position
Keep the header at the top of page when we scroll
keep the side bar at the top of the page
and also whenever we see any element at the top of other element  that is by the help of the css position


Css position add another dimension to your page


static is the Default layout to be applied
Position Fixed is a way of fixing the Header to the top 
and there are top bottom lift and right that you need to set if we need the change in size of the Header

top: 0 : 0 px with the top of the browser window
How far our element is from window
let: 0 How much is the edge form the left of the window

A special feature of this property is that if we set it in opposite directions the element will stretch



but if not hieght and width can be added 

To have good distance between the other content and header then you can add the body with padding-top

----------------------------------------------------------------------------------------------------------------------
Lesson 15:
Position Absolutr and Position Relative

Position Absolute also takes the same value as fixed that is top, bottom, left, width
Its like the position fixed
but key difference: 
fixed = placed in the browser window
absolute = placed on the page


Position Absoutle once the Page moves it will move with the page
Position fix position the element into the browser
Position Absolute position the element on the page

The Element written below is going to appear in front of the Elements that are written above it we can overide this with 
z-index:1

The elements with higher z-index will apear in front 
The one which has higher z-index will apear first 



Position static always appear at the back



----------------------------------------------------------------------------------------------------------------------








https://www.youtube.com/watch?v=G3e-cpL7ofc&t=11717s
