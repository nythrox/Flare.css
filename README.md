Flare.css
Flare is a modern CSS library that allows you to create responsive layouts with less code.

Automatic Responsiveness and Manual Responsiveness
Flare can handle responsiveness automatically but also gives you the option to manually control it.

When creating a layout, you have the option to define all column sizes on breakpoints, to let Flare handle the sizes, or to combine both and let Flare handle sizes but overwrite them on certain breakpoints.

Block layout and Flex layout
Flare adds features so you can make different types of layouts that are not supported on other frameworks. You can build with block layout or flex layout depending on your needs or even combine both.

More Containers, More sizes
Flare gives you many different sized containers, you can choose between container, container fluid, container small, container medium, container-one up to container-sixteen and customizable sizes on each breakpoint.

Light & Fast code, Faster workflows
Flare's main objective is to allow you to build websites faster, with lighter code and without restricting you or making your website heavy.

You set the size you wish the columns to be on desktop and flare will find an ideal size for them on other devices.

Column
Columns are the building blocks of flare. We give them sizes and add content inside of them.

Flare can have up to 16 columns in each row.

A column can have a size of one to sixteen, one being 6.25% of the container and sixteen being 100%.

You define the sizes of the columns on each device by using the tags m (mobile), t (tablet), c (computer).

For each breakpoint you choose, the size you set counts for itself and up. Example: t-ten will mean the column will have size 10 on tablets, computers and up.

Alternatively, you can let flare handle responsiveness by defining the sizes of the columns without a breakpoint prefix (column eight instead of column c-eight). If you want to change the size on a certain breakpoint, you can add breakpoint tags and they will only count for them self. Example: t-ten will set the column to the size ten on tablet only, while flare chooses the size on other screens.

To combine automatic with manual responsiveness, you can choose automatic responsiveness and then overwrite it on specific breakpoints. Example: column eight t-eight means that flare will handle responsiveness on all devices except tablets, where the column will take the size of eight.

When using breakpoints in combination with automatic responsiveness, breakpoints no longer count for themselves and up, they count only for themselves. Example: column twelve t-sixteen instead of t-sixteen counting for tablet and up, it will only give the column size 16 at tablet.

Using the tag column is not obligatory, but it's ideal for easy CSS targeting

Tags to put in a column
(breakpoint-)number

self-grow (horizontally)
self-nogrow (horizontally)
self-stretch (vertically)
self-nostretch (vertically)
self-shrink (horizontally)
self-noshrink (horizontally)
self-left
self-right
self-top
self-middle (horizontally)
self-bottom
fill
auto
title
self-mx-auto
no-gutter
Tags to put in a container that modify columns
(breakpoint-)equal-number
grow (horizontally)
nogrow (horizontally)
stretch (vertically)
nostretch (vertically)
shrink (horizontally)
noshrink (horizontally)
left
center
right
space-around
space-between
top
middle (horizontally)
bottom
normal
content-stretch
content-middle
content-bottom
content-top
self-no-gutter
Container
Containers are used to set items side by side.

With a container, you can define the size of the container and the size of the columns inside of it (unless they get overwritten)

They can also be used to limit the total size of the content, centralizing it in the screen.

Inside of containers, columns behave with a block behavior.

Block behavior: Collumns will have defined sizes that will not grow or shrink, and their content will fit inside them.

Container attributes:

container
fluid, small, medium
size-number
breakpoint-size-number

row
nomax
fullheight
singleline
Flexbox
Flexboxes are used to set items side by side.

Inside of flexbox, columns behave with a flex behavior.

Flex behavior: Collumns will be sized according to their contents, and will always try to grow to fill 100% of the empty space. Columns are more flexible, they will never have an exactly specific width even if you add width attributes.

Flexbox attributes:

multiline
equal
size-number
breakpoint-size-number
equal-number
breakpoint-equal-number
Automatic Responsiveness
When giving a column a certain size column eight , you tell flare that you want it's size to be eight (half) at a computer screen, and flare will handle responsiveness on tablet and mobile.


If you dont like the result on a certain screen size, you can always add a extra modifier column eight t‑twelve ‑ Flare will handle on mobile, but on tablet it will have the size of twelve


Or if you dont want to use automatic responsiveness at all, you can build from mobile up using the breakpoint tags column m‑sixteen t‑fourteen c‑twelve Without automatic responsiveness, each breakpoint tag counts for itself and up (Example: t‑eight will make the column size eight for tablet, computer, television, etc)

Attributes:
Column

container and flexbox

Tags to put in a column
(breakpoint-)number

self-grow (horizontally)
self-nogrow (horizontally)
self-stretch (vertically)
self-nostretch (vertically)
self-shrink (horizontally)
self-noshrink (horizontally)
self-left
self-right
self-top
self-middle (horizontally)
self-bottom
(breakpoint-)first
(last-)first
fill
auto
title
self-mx-auto
no-gutter
(last-)break
Tags to put in a container that modify columns
(breakpoint-)equal-number
grow (horizontally)
nogrow (horizontally)
stretch (vertically)
nostretch (vertically)
shrink (horizontally)
noshrink (horizontally)
left
center
right
space-around
space-between
top
middle (horizontally)
bottom
normal
content-stretch
content-middle
content-bottom
content-top
self-no-gutter
Container attributes:

container
fluid, small, medium
size-number
breakpoint-size-number

row
nomax
fullheight
(breakpoint-)singleline
all-center
items-centralized
content-centralized
Flexbox attributes:

multiline
equal
size-number
breakpoint-size-number
equal-number
breakpoint-equal-number
other attributes

(breakpoint-)text-center
