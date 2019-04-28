# Flare.css
Flare is a modern CSS library that allows you to create responsive layouts with less code.
<h2>Automatic Responsiveness and Manual Responsiveness</h2>
<p>
Flare can handle responsiveness automatically but also gives you the option to manually control it.
</p>
<p>When creating a layout, you have the option to define all column sizes on breakpoints, to let Flare handle the sizes, or to combine both and let Flare handle sizes but overwrite them on certain breakpoints.</p>
<h2>Block layout and Flex layout</h2>
<p>Flare adds features so you can make different types of layouts that are not supported on other frameworks. You can build with block layout or flex layout depending on your needs or even combine both.</p>
<h2>More Containers, More sizes</h2>
<p>Flare gives you many different sized containers, you can choose between container, container fluid, container small, container medium, container-one up to container-sixteen and customizable sizes on each breakpoint.</p>

<h2>Light & Fast code, Faster workflows</h1>
<p>Flare's main objective is to allow you to build websites faster, with lighter code and without restricting you or making your website heavy. </p>
<p>You set the size you wish the columns to be on desktop and flare will find an ideal size for them on other devices.</p>
<h1>Column</h2>
<p>
Columns are the building blocks of flare. We give them sizes and add
content inside of them.
</p>
<P>Flare can have up to 16 columns in each row.</P>
<p>
A column can have a size of one to sixteen, one being 6.25% of the
container and sixteen being 100%.
</p>
<p>You define the sizes of the columns on each device by using the tags m (mobile), t (tablet), c (computer). </p>
<p>For each breakpoint you choose, the size you set counts for itself and up. Example: <code>t-ten</code> will mean the column will have size 10 on tablets, computers and up.</p>
<p>Alternatively, you can let flare handle responsiveness by defining the sizes of the columns without a breakpoint prefix (<code>column eight</code> instead of <code>column c-eight</code>). If you want to change the size on a certain breakpoint, you can add breakpoint tags and they will only count for them self. Example: <code>t-ten</code> will set the column to the size ten on tablet only, while flare chooses the size on other screens.</p>
<p>To combine automatic with manual responsiveness, you can choose automatic responsiveness and then overwrite it on specific breakpoints. Example: <code>column eight t-eight</code> means that flare will handle responsiveness on all devices except tablets, where the column will take the size of eight.</p>
<P>When using breakpoints in combination with automatic responsiveness, breakpoints no longer count for themselves and up, they count only for themselves. Example: <code>column twelve t-sixteen</code> instead of t-sixteen counting for tablet and up, it will only give the column size 16 at tablet.</P>
<p>Using the tag column is not obligatory, but it's ideal for easy CSS targeting</p>

<h4>Tags to put in a column</h4>
<ul>
  <li>(breakpoint-)number</li>
  <br>
  <li>self-grow (horizontally)</li>
  <li>self-nogrow (horizontally)</li>
  <li>self-stretch (vertically)</li>
  <li>self-nostretch (vertically)</li>
  <li>self-shrink (horizontally)</li>
  <li>self-noshrink (horizontally)</li>
  <li>self-left</li>
  <li>self-right</li>
  <li>self-top</li>
  <li>self-middle (horizontally)</li>
  <li>self-bottom</li>
  <li>fill</li>
  <li>auto</li>
  <li>title</li>
  <li>self-mx-auto</li>
  <li>no-gutter</li>
  </ul>
<h4>Tags to put in a container that modify columns</h4>
<ul>
  <li>(breakpoint-)equal-number</li>
  <li>grow (horizontally)</li>
  <li>nogrow (horizontally)</li>
  <li>stretch (vertically)</li>
  <li>nostretch (vertically)</li>
  <li>shrink (horizontally)</li>
  <li>noshrink (horizontally)</li>
  <li>left</li>
  <li>center</li>
  <li>right</li>
  <li>space-around</li>
  <li>space-between</li>
  <li>top</li>
  <li>middle (horizontally)</li>
  <li>bottom</li>
  <li>normal</li>
  <li>content-stretch</li>
  <li>content-middle</li>
  <li>content-bottom</li>
  <li>content-top</li>
  <li>self-no-gutter</li>
</ul>
<h1>Container</h1>
<p>Containers are used to set items side by side.</p>
<p>With a container, you can define the size of the container and the size of the columns inside of it (unless they get overwritten)</p>
<p>They can also be used to limit the total size of the content, centralizing it in the screen.</p>
<p>Inside of containers, columns behave with a block behavior.</p>
<p>Block behavior: Collumns will have defined sizes that will not grow or shrink, and their content will fit inside them.</p>
<p>Container attributes:</p>
<ul>
  <li>container</li>
  <li>fluid, small, medium</li>
  <li>size-number</li>
  <li>breakpoint-size-number</li>
  <br>
  <li>row</li>
  <li>nomax</li>
  <li>fullheight</li>
  <li>singleline</li>
</ul>

<h1>Flexbox</h1>
<p>Flexboxes are used to set items side by side.</p>
<p>Inside of flexbox, columns behave with a flex behavior.</p>
<p>Flex behavior: Collumns will be sized according to their contents, and will always try to grow to fill 100% of the empty space. Columns are more flexible, they will never have an exactly specific width even if you add width attributes.</p>
<p>Flexbox attributes:</p>
<ul>
<li>multiline</li>
<li>equal</li>
<li>size-number</li>
<li>breakpoint-size-number</li>
<li>equal-number</li>
<li>breakpoint-equal-number</li>
</ul>
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
<ul>
  <li>(breakpoint-)number</li>
  <br>
  <li>self-grow (horizontally)</li>
  <li>self-nogrow (horizontally)</li>
  <li>self-stretch (vertically)</li>
  <li>self-nostretch (vertically)</li>
  <li>self-shrink (horizontally)</li>
  <li>self-noshrink (horizontally)</li>
  <li>self-left</li>
  <li>self-right</li>
  <li>self-top</li>
  <li>self-middle (horizontally)</li>
  <li>self-bottom</li>
  <li>(breakpoint-)first</li>
  <li>(last-)first</li>
  <li>fill</li>
  <li>auto</li>
  <li>title</li>
  <li>self-mx-auto</li>
  <li>no-gutter</li>
  <li>(last-)break</li>
  </ul>
<h4>Tags to put in a container that modify columns</h4>
<ul>
  <li>(breakpoint-)equal-number</li>
  <li>grow (horizontally)</li>
  <li>nogrow (horizontally)</li>
  <li>stretch (vertically)</li>
  <li>nostretch (vertically)</li>
  <li>shrink (horizontally)</li>
  <li>noshrink (horizontally)</li>
  <li>left</li>
  <li>center</li>
  <li>right</li>
  <li>space-around</li>
  <li>space-between</li>
  <li>top</li>
  <li>middle (horizontally)</li>
  <li>bottom</li>
  <li>normal</li>
  <li>content-stretch</li>
  <li>content-middle</li>
  <li>content-bottom</li>
  <li>content-top</li>
  <li>self-no-gutter</li>
</ul>
<p>Container attributes:</p>
<ul>
  <li>container</li>
  <li>fluid, small, medium</li>
  <li>size-number</li>
  <li>breakpoint-size-number</li>
  <br>
  <li>row</li>
  <li>nomax</li>
  <li>fullheight</li>
  <li>(breakpoint-)singleline</li>
  <li>all-center</li>
  <li>items-centralized</li>
  <li>content-centralized</li>
</ul>
<p>Flexbox attributes:</p>
<ul>
<li>multiline</li>
<li>equal</li>
<li>size-number</li>
<li>breakpoint-size-number</li>
<li>equal-number</li>
<li>breakpoint-equal-number</li>
</ul>
<p>other attributes</p>
<ul>
  <li>(breakpoint-)text-center</li>
</ul>
