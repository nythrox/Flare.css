# Flare.css
Lightweight CSS Layout framework
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600"
      rel="stylesheet"
    />
    <link type="text/css" rel="stylesheet" href="reset.css" />
    <link type="text/css" rel="stylesheet" href="container.css" />
    <link type="text/css" rel="stylesheet" href="flare.css" />
    <link type="text/css" rel="stylesheet" href="column.css" />
    <link type="text/css" rel="stylesheet" href="flexbox.css" />
    <link type="text/css" rel="stylesheet" href="ui.css" />
    <link type="text/css" rel="stylesheet" href="theme.css" />
    <link rel="icon" href="flare.png" />

    <style>
      .menu {
        border-right: 1px solid rgba(0, 0, 0, 0.14);  
        position:fixed;
      }
      @media (max-width:767px) {
      .menu {  
        position:static;
        height:auto;
        padding:0px!important;
        border-right:none;
        border-bottom:1px solid rgba(0,0,0,0.14);
      }

      }
      .menu ul {
        list-style:none!important;
      }
      .menu ul li:first-child {
        border-top: 1px solid rgba(0, 0, 0, 0.14);
      }
      .menu ul li {
        margin-left: 0px!important;
        padding: 15px 20px;
      }
      .menu ul li:hover {
        background-color: rgba(0, 0, 0, 0.05);
      }
      .logo {
        text-align: center;
      }
      .menu hr {
        margin: 0px;
      }
      .logo img {
        width: 75px;
        margin-top: 25px;
      }
      section {
        margin: 0px;
        padding-top: 50px !important;
        padding-bottom: 50px !important;
      }
      #content section:not(:first-child) {
        border-top: 1px solid black;
      }
      .welcome {
        border-top: none !important;
        padding-top: 0px !important;
      }
      .example .column {
        padding: 10px 0;
        text-align: center;
        border:1px solid white;
      }
      .example .column:nth-child(even) {
        background: tomato;
      }
      .example .column:nth-child(odd) {
        background: skyblue;
      }
      .example .title {
        background: white !important;
      }
      .example .title h2 {
        margin-top: 0px;
        margin-bottom: 0px;
      }
      :not(.menu) ul {
        list-style: circle;
      }
      :not(.menu) ul li{
          margin-left:20px;
      }
      code {
          background:rgba(199, 199, 199, 0.541);
          border-radius:3px;
          padding:2px 2px;
          font-family:"Courier New", Courier, monospace	;
      }
    </style>
  </head>
  <body> 
    <section class="menu fullheight t-three m-full">
      <ul>
          <li>Grid</li>
          <li>Introduction</li>
      </ul>
    </section>
    <div class="container t-thirteen t-offset-left-three" id="content">
        <section class="part"> 
          <h1>Introduction</h1>
          <p>
            The idea behind flare is to be able to let you program layouts with less lines of code and give you more options for building, without limiting you in any ways or making your website slow.
          </p>
          <p>
            Automatic Responsiveness, Flexbox, different containers, being lightweight and short readable code are the main differencials that flare has from bootstrap, but they are all optional and do not restrict or limit how you program, or interfere with other frameworks..
          </p>
          <br />
        </section>
        <section class="part">
          <h1>Column</h1>
          <p>
            Columns are the building blocks of flare. We give them sizes and add
            content inside of them.
          </p>
          <P>Flare can have up to 16 columns in each row.</P>
          <div class="example container ">
            
              <div class="column m-sixteen">16</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
              <div class="column m-one">1</div>
          </div>
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
          <div class="container fluid example">
            <div class="column nine">nine</div>
            <div class="column seven">seven</div>
          </div>
          <div class="container fluid text-center">
            <div class="column title">
              <h4>container equal-three</h4>
            </div>
          </div>
          <div class="example container equal-three">
            <div class="column">column</div>
            <div class="column">column</div>
            <div class="column">column</div>
          </div>
          <h1>Manual Responsiveness (bootstrap-like)</h1>
          <p>You define the sizes of the columns on each device by using the tags m (mobile), t (tablet), c (computer). </p>
          <p>For each breakpoint you choose, the size you set counts for itself and up. Example: <code>t-ten</code> will mean the column will have size 10 on tablets, computers and up.</p>
          <div class="container fluid example">
            <div class="column m-sixteen c-nine">m-sixteen t-nine</div>
            <div class="column m-sixteen c-seven">m-sixteen t-seven</div>
          </div>
          <div class="container fluid text-center">
            <div class="column title">
              <h4>container m-equal-one t-equal-three</h4>
            </div>
          </div>
          <div class="example container m-equal-one c-equal-three">
            <div class="column">column</div>
            <div class="column">column</div>
            <div class="column">column</div>
          </div>  <h1>Combining both</h1>
          <p>You can choose a automatic responsiveness and then overwrite it on specific breakpoints. Example: <code>column eight t-eight</code> means that flare will handle responsiveness on all devices exept tablets, where the column will take the size of eight.</p>
          <P>When using breakpoints in combination with automatic responsiveness, breakpoints no longer count for themselves and up, they count only for themselvs. Example: <code>column twelve t-sixteen</code> instead of t-sixteen counting for tablet and up, it will only give the column size 16 at tablet.</P>
        </section>
        
        <section class="part">
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
      
                <br />
                <div class="container fluid text-center">
                  <div class="column title"><h2>container fluid</h2></div>
                </div>
                <div class="container fluid example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
                <div class="container fluid text-center">
                  <div class="column title"><h2>container</h2></div>
                </div>
                <div class="container example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
                <div class="container fluid text-center">
                  <div class="column title"><h2>container medium</h2></div>
                </div>
                <div class="container medium example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
                <div class="container fluid text-center">
                  <div class="column title"><h2>container small</h2></div>
                </div>
                <div class="container small example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
                <div class="container fluid text-center">
                  <div class="column title">
                    <h2>container size-ten</h2>
                    <p>
                      has a size of ten on computer and up, while letting flare handle
                      mobile and tablet
                    </p>
                  </div>
                </div>
                <div class="container size-ten example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
                <div class="container fluid text-center">
                  <div class="column title">
                    <h2>container m-size-twelve t-size-ten c-size-eight</h2>
                    <p>
                      will have a size of twelve on mobile, and a size of ten on
                      tablet and a size of eight on computer and up
                    </p>
                  </div>
                </div>
                <div class="container m-size-twelve t-size-ten c-size-eight example">
                  <div class="column half">half</div>
                  <div class="column half">half</div>
                </div>
              </section>
        <section class="part">
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
          <br>
          <div class="example">
                <div class="container fluid text-center">
                  <div class="column title"><h2>flexbox</h2>all the columns
                    resize
                    according to the
                    size
                    of their content
                    unless you add a number
                </div>
              <div class="flexbox">
                    <div class="column">all the columns</div>
                    <div class="column">resize</div>
                    <div class="column">according to the</div>
                    <div class="column">size</div>
                    <div class="column">of their content</div>
                    <div class="column six">(six) unless you add a number</div>
              </div>
            </div>
            
          <br>
          <div class="example">
                <div class="container fluid text-center">
                  <div class="column title"><h2>flexbox equal</h2>
                <p>columns no longer adapt to the size of their content, but now they will always have an equal size</p></div>
                </div>
              <div class="flexbox equal">
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column space text bla bla bla</div>
                    <div class="column">column</div>
              </div>
            </div>
             
          <br>
          <div class="example">
                <div class="container fluid text-center">
                  <div class="column title"><h2>flexbox m-equal-three multiline</h2>
                <p>from mobile and up will each line have three columns, and when overflowing the columns will break into a new line</p></div>
                </div>
              <div class="flexbox m-equal-three multiline">
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column</div>
                    <div class="column">column space text bla bla bla</div>
                    <div class="column">column</div>
              </div>
            </div>
        </section>
        <section class="part">
            <h1>Automatic Responsiveness</h1>
            <p>When giving a column a certain size <code>column eight</code> , you tell flare that you want it's size to be eight (half) at a computer screen, and flare will handle responsiveness on tablet and mobile.</p>
            <br>
            <p>If you dont like the result on a certain screen size, you can always add a extra modifier <code>column eight t&#8209;twelve</code> &#8209; Flare will handle on mobile, but on tablet it will have the size of twelve</p>
            <br>
            <p>Or if you dont want to use automatic responsiveness at all, you can build from mobile up using the breakpoint tags <code>column m&#8209;sixteen t&#8209;fourteen c&#8209;twelve</code> Without automatic responsiveness, each breakpoint tag counts for itself and up (Example: t&#8209;eight will make the column size eight for tablet, computer, television, etc)</p>
        </section>
        
        <section class="part">
                <h1>How to Build, Guidelines, Best Practices</h1>
                <p>Without using automatic responsiveness (bootstrap-like), build from mobile-up.</p>
                <p>Using automatic responsiveness, build from the computer down if you need to change a size.</p>
                <br>
                <p>Wrap all your Main content in a container flex or a container</p>
                <p>using the tag column is optional, but its ideal for easy css targeting</p>
                <p></p>
            </section>
          
        <section class="part">
                <h1>Attributes:</h1>
                <p>Column</p>
                <p>container and flexbox</p>
            </section>
            
    </div>
  </body>
</html>
