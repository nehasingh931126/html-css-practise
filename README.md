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





