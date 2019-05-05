<h1> Flare.css</h1>
Flare is a modern CSS library that allows you to create responsive layouts with less code. Flare also gives you faster and better ways to create layouts, but doesn't impose on the way you have to code.

<h2>Automatic Responsiveness and Manual Responsiveness</h2>
<p>
Flare can handle responsiveness automatically but also gives you the option to manually control it.
</p>
<p>When creating a layout, you have the option to define all column sizes on certain breakpoints, or to define the column sizes only on computer and let Flare handle the sizes on other breakpoints, or to combine both and let Flare handle sizes but overwrite them on certain breakpoints.</p>

<h2>Block layout and Flex layout</h2>
<p>Flare adds features so you can make different types of layouts that are not supported on other frameworks. You can build with block layout or flex layout depending on your needs and you can also combine both, getting only the parts of each that you need.</p>

<h2>More Containers</h2>
<p>Flare gives you many different sized containers, you can choose between container, container fluid, container small, container medium, container-one up to container-sixteen and customizable sizes on each breakpoint.</p>

<h2>Light & Fast code, Faster workflows</h1>
<p>Flare's main objective is to allow you to build websites faster, with lighter code and without restricting you or making your website heavy. </p>
<p>You set the size you wish the columns to be on desktop and flare will find an ideal size for them on other devices.</p>
<br>

<h2>Better Tablet responsiveness</h2
<p>Flare adapts container sizes so items look better on tablets and small computers.</p>

<h1>Documentation</h1>
<h2>Breakpoints</h2>
<p>the breakpoints are:</p>
<ul>
  <li>m (mobile)</li>
  <li>t (tablet)</li>
  <li>c (computer)</li>
  <li>lg</li>
  <li>xl</li>
  <li>xxl</li>
</ul>
<code>
@media(max-width:768px) {
}
</code>
<code>
@media(min-width:768px) and (max-width:900px){
}
</code>
<code>
@media(min-width:901px) and (max-width:1149px){
}
</code>
<code>
@media(min-width:1150px) and (max-width:1649px){
}
</code>
<code>
@media(min-width:1650px) and (max-width:2999px){
}
</code>
<code>
@media(min-width:3000px){
}
</code>
<h2>Priority</h2>
When you have multiple tags trying to define the size of a column, what tag will the column obey? THe tag with the highest priority number. If its a zero then it wont follow any and will go to default width (row or flexbox default)
[building using automatic responsiveness]: 
first you set a automatic value, then you tweak it on certain breakpoints if needed
if you set a equal-number value, if you want to overrite it on column (number, breakpoint-number) then you will treak it on certain breakpoints

<h2>Column</h2>
<p>
Columns are the building blocks of flare. We can give them sizes and add
content inside of them. Their default behavior depends if they are in a row or a flexbox.
</p>
<p>
A column can have a size of one to sixteen, *one* being 6.25% of the
container, *eight* being 50%, *sixteen* being 100% and so on.
</p>
<p>You define the sizes of the columns on each device by using the tags m (mobile), t (tablet), c (computer). </p>
<p>For each breakpoint you choose, the size you set counts for itself and up. Example: <code>t-ten</code> will mean the column will have size 10 on tablets, computers and up.</p>
<p>Alternatively, you can let flare handle responsiveness by defining the sizes of the columns without a breakpoint prefix (<code>column eight</code> instead of <code>column c-eight</code>). If you want to change the size on a certain breakpoint, you can add breakpoint tags and they will only count for them self. Example: <code>t-ten</code> will set the column to the size ten on tablet only, while flare chooses the size on other screens.</p>
<p>To combine automatic with manual responsiveness, you can choose automatic responsiveness and then overwrite it on specific breakpoints. Example: <code>column eight t-eight</code> means that flare will handle responsiveness on all devices except tablets, where the column will take the size of eight.</p>
<P>When using breakpoints in combination with automatic responsiveness, breakpoints no longer count for themselves and up, they count only for themselves. Example: <code>column twelve t-sixteen</code> instead of t-sixteen counting for tablet and up, it will only give the column size 16 at tablet.</P>
<p>Using the tag <code>column</code> is not obligatory, but it's ideal for easy CSS targeting</p>
<p>Main sizing tags for columns: number*, equal-number*, equal*</p>
<p>Main alignment tags for columns: first*, last*, self-left, self-right, self-top, self-bottom, self-middle, stretch, grow, shrink</p>

* = has breakpoints (m- t- c- lg- xl- xxl-), if using not using breakpoint then flare handles its responsiveness

<h1>Row & Flexbox</h1>
<p>Rows & Flexboxes are used to set items side by side.</p>
<p>You can add a size to the row to limit the total size of the content, centralizing it in the screen.</p>

<p>Inside of rows, columns behave with a block behavior.</p>
<p>Inside of flexbox, columns behave with a flex behavior.</p>
<h4>Block behavior: </h4>
  Collumns will have defined sizes that will not grow or shrink. <br>
  Columns in a line have the same vertical size (stretch). <br>
  Columns overflowing will jump to the next line.<br>


<h4>Flex behavior: </h4>
  Collumns are sized acording to the size of their content (width:auto). <br>
  Columns in a line have the same vertical size (stretch). <br>
  Columns will grow to fill all empty space. <br>
  Columns will shrink to fit in one line.</p><br>
  
<p>All default behaviors can be overwritten with tags (see column tags), and are only here to facilitate development</p>

Container Sizes: container, fluid, small, medium, size-number*
<br>
Overwrite behavior tags: grow, stretch, shrink, singleline, multiline, size-number*, equal*, equal-number*
<br>
* = has breakpoints (m- t- c- lg- xl- xxl-), if using not using breakpoint then flare handles its responsiveness

<h1>Automatic Responsiveness</h1>
<p>When giving a column a certain size <code>column eight</code> , you tell flare that you want it's size to be eight (half) at a computer screen, and flare will handle responsiveness on tablet and mobile.</p>
<br>
<p>If you dont like the result on a certain screen size, you can always add a extra modifier <code>column eight t&#8209;twelve</code> &#8209; Flare will handle on mobile, but on tablet it will have the size of twelve</p>
<br>
<p>Or if you dont want to use automatic responsiveness at all, you can build from mobile up using the breakpoint tags <code>column m&#8209;sixteen t&#8209;fourteen c&#8209;twelve</code> Without automatic responsiveness, each breakpoint tag counts for itself and up (Example: t&#8209;eight will make the column size eight for tablet, computer, television, etc)</p>

<h1>Attributes:</h1>
<p>Column</p>
<p>container and flexbox</p>
<h4>Tags to put in a column</h4>
* = has breakpoints (m- t- c- lg- xl- xxl-)
<br>

self positive | self negative | group positive | group negative
------------- | ------------- | ------------- | -------------
self-grow | self-nogrow | grow | nogrow
self-stretch | self-nostretch | stretch | nostretch
self-shrink | self-noshrink | shrink | noshrink

<h2>Horizontal Positioning</h2>
* = has breakpoints (m- t- c- lg- xl- xxl-)
<br>

self | group
------------- | -------------
self-left | left
self-right | right
first* | ---
last* | ---
--- | center
--- | space-around
--- | space-between
--- | normal
self-mx-auto | mx-auto

<h2>Vertical Positioning</h2>

self        | group
--------    | -----
self-top    | top
self-bottom | bottom
self-middle | middle
 | content-top
 | content-bottom
 | content-middle
 | content-stretch
 
<h2>Column Sizing</h2>

tag | description
------ | ------
number* | column size on * breakpoint. number can be any value from one to sixteen
fill | occupies all empty space
auto | size according to its content
title | always 100% width
break* | breaks the line
self-no-gutter | will have no gutter

<h4>Tags to put in a container that modify columns</h4>

tag | description
------ | ------
equal-number* | number of columns on * breakpoint inside this row. number can be any value from one to twelve
flexbox | columns inside thsi row will behave with flex behavior
equal* | columns inside this row will all have an equal width
no-gutter | columns inside this row will have no gutter
all-center | text-center, columns centered vertically and horizontaly
items-centralized | columns centered vertically and horizontaly
content-centralized | content centered vertically and horizontaly

<p>Row and Flexbox attributes:</p>

tag | description
------ | ------
row | columns inside this row will have default block behavior
flexbox | columns inside this flexbox will have default flex behavior
container, fluid, small, medium | different sized containers
size-number* | defines the size of the container. number can be any value from one to sixteen
singleline* | on * breakpoint, row will be a single line
multiline* | flexbox can have multiple lines
fullheight | will have a 100vh height
nomax | will have no max width 

<h1>Other Attributes</h1>

tag | description
------ | ------
text-center* | on * brekapoint text will be centralized 
hide* | on * breakpoint the item will be hidden

<h1>Browser Support</h1>
<ul>
  <li>Last 2 Versions FF, Chrome, Safari Mac</li>
<li>IE 11+</li>
<li>Android 4.4+, Chrome for Android 44+</li>
<li>iOS Safari 7+</li>
<li>Microsoft Edge 12+</li>
</ul>
