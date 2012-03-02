# jQuery Flip Plugin

jQuery/jQuery mobile plugin to give Flipboard app like effect. Flip effect uses css 3d transform. Flip effect currently works on WebKit browsers (e.g. Chrome, Safari, including iOS mobile safari) or Firefox 11. Other browsers will be fallback to "slide" effect.


## Installation

Copy jquery.mobile.flip.js, jquery.mobile.flip.css and images directory to your web page project. Note that css file and images folder must be in the same directory. 

After copying files to your web project, load js and css file into your html.

    <!-- "images" directory must be copied under css folder -->
    <link rel="stylesheet" href="css/jquery.mobile.flip.css" />
    <script type="text/javascript" src="js/jquery.mobile.flip.js"></script>

## Usage

### Prerequisite
This plugin expects nested div or p or section element structure. Page root div, p, section element must be used to initialize plugin.

    <div id="flipRoot">
       <!-- div element -->
       <div>
         Flip Content 1
       </div> 
       <!-- or p element -->
       <p> 
         Flip Content 2
       </p>
       <!-- or section element -->       
       <section>
         <h3>Flip Content 3</h3>
         <p>You can put any elements under here</p>
       </section>
    </div>

### jQuery User
jQuery user can enable plugin by calling jQuery.flip() method.

    $(document).ready(function() {
      $("#flipRoot").flip();
    });

option object can be passed to the flip() method like below. Available options are described later.

    $(document).ready(function() {
      $("#flipRoot").flip({
        forwardDir: "ltor",
        height: "340px",
        showpager: true,
        loop: true}));
    });

### jQuery Mobile User
Plugin will be initialized with the element which has data-role="flip" attribute without calling initialization method. 

    <div id="flipRoot" data-role="flip">
       <div>
         Flip Content 1
       </div> 
       <p> 
         Flip Content 2
       </p>
       <section>
         Flip Content 3
       </section>
    </div>

Option can be passed through data-flip- prefix attribute too.

    <div id="flipRoot" data-role="flip"  data-flip-show-pager="true" data-flip-forward-dir="ltor">
       <div>
         Flip Content 1
       </div> 
       <p> 
         Flip Content 2
       </p>
       <section>
         Flip Content 3
       </section>
    </div>

## Option
Following option is supported.

 option name | description | jqm attribute | value
-------------|-------------|---------------|------
effect       |Transiton effect|data-flip-effect|'flip' or 'slide'
forwardDir   |forward direction|data-flip-forward-dir|'rtol' or 'ltor' or 'ttob' or 'btot'
height       |Content height|data-flip-height| height css
keyboardNav  |enable keyboard navigation|data-flip-keyboard-nav|true or false
showPager    |show pager|data-flip-show-pager|true or false
loop         |loop contents|data-flip-loop|true or false

Sample:

    $(document).ready(function() {
      $("#flipRoot").flip({
        forwardDir: 'ltor',
        height: '340px',
        showpager: true,
        loop: true}));
    });
    
    <div id="flipRoot" data-role="flip"  data-flip-show-pager="true" data-flip-forward-dir="ltor">
       <div>
         Flip Content 1
       </div> 
       <p> 
         Flip Content 2
       </p>
       <section>
         Flip Content 3
       </section>
    </div>
    

## License

[The MIT License](http://www.opensource.org/licenses/mit-license.php "link to Open Source Initiative")
