# sheet priority
There are three main ways to insert style sheet.
1. External style sheet
2. Internal style sheet
3. Inline style sheet

the priority is **3>2>1**

# link style (_a_ tag)
there are four states in it.
1. a:link
2. a:visited
3. a:hover
4. a:active

# differrence between <font color="#ff3333"> :: </font> and <font color="#0033ff"> : </font>
in general __::__ is used to indicate a <em>pseudo-element</em>,  __:__ represents <em>pseudo-class</em>.
if there is not a dom in your html, then you can not bind a event to it.

# px and rem relation
1rem = per unit font-size in html    

# indicate the CSS height and width value means the content width and height. (exclude the padding and margin)
If the height value is less than the font-size value.Then the text could not be showed completely.

# It is necessary to use <em> .rem </em> all over the HTML when you transform px to rem in <u>html tag </u>

# woff = Web Open Font Format

# In general, we mainly use flow position display to regulate the tag position

# @font-face provides the current font library

# the difference between em and rem.
em could constantly find its fathet then get a value.
if we use tag in a recursing way. Then calculate the px value by em could be awful.On the contrary, using rem could be perfect.Because computing the px value by rem is simple--just multiply the html tag value with rem value.   

# background attributes are really many.
background-size background-position

# display and position and float overflow are important to regulate the element position
display can be flex block inline inline-block

# ellipsis attribute
``` text-overflow=ellipsis ```

# canvas tag
## change the canvas area
Please change the canvas attribute(width height) and not change the css style(px)

# response settings
use @media
Pay attention to change the body position.

# modify css problem
1. ## use ctrl+shift+c select a element
2. ## delete the element from stem to stern and observe the page diversification
   watch out: x scroll could influence y scroll

# z-index settings
if you want to set an item is in front of another, you'd better set the property on the brother level.

# /deep/ 
use this to figure out indicated compponent class.

# Layouts
## one should pay more attention to grid and flex
Because flex and frid are really more friendly.

### About flex
```flex-grow: 1 ``` means expand the space.(When other items all have the default value 0)