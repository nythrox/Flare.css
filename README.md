# Flare.css
Flare is a modern CSS library that allows you to create responsive layouts with less code.
<h2>Automatic Responsiveness</h2>
<p>
Flare handle responsiveness automatically, but also gives you the option to manually control it.
</p>
<p>
Automatic Responsiveness, Flexbox, different containers, being lightweight and short readable code are the main differencials that flare has from bootstrap, but they are all optional and do not restrict or limit how you program, or interfere with other frameworks..
</p>
<h1>Column</h1>
<p>
Columns are the building blocks of flare. We give them sizes and add
content inside of them.
</p>
<P>Flare can have up to 16 columns in each row.</P>
<p>
A column can have a size of one to sixteen, one being 6.25% of the
container and sixteen being 100%.
</p>
<p>Flexbox attributes:</p>
<ul>
<li>number</li>
<li>breakpoint-number</li>
<br>
<li>equal-number</li>
<li>breakpoint-equal-number</li>
</ul>
<h1>Automatic Responsiveness</h1>
<p>You set the size you wish the columns to be on desktop and flare will find a ideal size for them on other devices.</p>
<h1>Manual Responsiveness (bootstrap-like)</h1>
<p>You define the sizes of the columns on each device by using the tags m (mobile), t (tablet), c (computer). </p>
<p>For each breakpoint you choose, the size you set counts for itself and up. Example: <code>t-ten</code> will mean the column will have size 10 on tablets, computers and up.</p>
<h1>Combining both</h1>
<p>You can choose a automatic responsiveness and then overwrite it on specific breakpoints. Example: <code>column eight t-eight</code> means that flare will handle responsiveness on all devices exept tablets, where the column will take the size of eight.</p>
<P>When using breakpoints in combination with automatic responsiveness, breakpoints no longer count for themselves and up, they count only for themselvs. Example: <code>column twelve t-sixteen</code> instead of t-sixteen counting for tablet and up, it will only give the column size 16 at tablet.</P>
<h1>Container</h1>
<p>Containers are used to set items side by side.</p>
<p>With a container, you can define the size of the container and the size of the columns inside of it (unless they get overwritten)</p>
<p>They can also be used to limit the total size of the content, centralizing it in the screen.</p>
<p>Inside of containers, columns behave with a block behavior.</p>
<p>Block behavior: Collumns will have defined sizes that will not grow or shrink, and their content will fit inside them.</p>
<p>Container attributes:</p>
<ul>
  <li>container fluid</li>
  <li>container</li>
  <li>small, medium</li>
  <li>size-number</li>
  <li>breakpoint-size-number</li>
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
<h1>How to Build, Guidelines, Best Practices</h1>
<p>Without using automatic responsiveness (bootstrap-like), build from mobile-up.</p>
<p>Using automatic responsiveness, build from the computer down if you need to change a size.</p>
<br>
<p>Wrap all your Main content in a container flex or a container</p>
<p>using the tag column is optional, but its ideal for easy css targeting</p>
<p></p>
<h1>Attributes:</h1>
<p>Column</p>
<p>container and flexbox</p>
