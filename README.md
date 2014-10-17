# Buckeye Interactive Reveal.js Theme

This is the [Buckeye Interactive](http://www.buckeyeinteractive.com)-branded theme for [Reveal.js](https://github.com/hakimel/reveal.js). It's intended to be loaded via [Bower](http://bower.io/) when using the [Yeoman Reveal.js generator](https://github.com/slara/generator-reveal).

## Installation

1. Start a new Reveal.js project, using the [Reveal.js generator documentation](https://github.com/slara/generator-reveal#revealjs-generator) documentation as a guide.

2. Once installed, run `bower install https://github.com/buckii/buckii-reveal-theme.git` to download this theme into your presentation.

3. Load the Buckeye Interactive theme in css/source/theme.scss. You can also lose a lot of the default theme as well to save on loading time:

        - / Include theme-specific fonts ----------------
        - @font-face {
        -         font-family: 'League Gothic';
        -         src: url('../../bower_components/reveal.js/lib/font/league_gothic-webfont.eot');
        -         src: url('../../bower_components/reveal.js/lib/font/league_gothic-webfont.eot?#iefix') format('embedded-opentype'),
        -                  url('../../bower_components/reveal.js/lib/font/league_gothic-webfont.woff') format('woff'),
        -                  url('../../bower_components/reveal.js/lib/font/league_gothic-webfont.ttf') format('truetype'),
        -                  url('../../bower_components/reveal.js/lib/font/league_gothic-webfont.svg#LeagueGothicRegular') - format('svg');
        -
        -         font-weight: normal;
        -         font-style: normal;
        - }
        -
        - @import url(https://fonts.googleapis.com/css?family=Lato:400,700,400italic,700italic);
        - // ---------------------------------------------
        -
        - // Override theme settings ---------------------
        - $heading1TextShadow: 0 1px 0 #ccc, 0 2px 0 #c9c9c9, 0 3px 0 #bbb, 0 4px 0 #b9b9b9, 0 5px 0 #aaa, 0 6px 1px rgba(0,0,0,.1), - 0 0 5px rgba(0,0,0,.1), 0 1px 3px rgba(0,0,0,.3), 0 3px 5px rgba(0,0,0,.2), 0 5px 10px rgba(0,0,0,.25), 0 20px 20px rgba(0,0- ,0,.15);
        - // Other options include e.g.
        - // $mainFont: 'Open Sans', sans-serif;
        - // $linkColor: #ed1dff;
        - // $linkColorHover: $linkColor;
        - // $headingFont: 'Montserrat', Impact, sans-serif;
        - // $headingTextShadow: none;
        - // $headingLetterSpacing: -0.03em;
        - // $headingTextTransform: none;
        - // $selectionBackgroundColor: #e0ad52;
        - // $mainFontSize: 30px;
        - // See ../../bower_components/reveal.js/css/theme/template/settings.scss for the full list.
        - // ---------------------------------------------
        -
        - // Background generator ------------------------
        - @mixin bodyBackground() {
        -         @include radial-gradient( rgba(28,30,32,1), rgba(85,90,95,1) );
        - }
        - // ---------------------------------------------
        -
        + @import "../../bower_components/buckii-reveal-theme/bii-theme.scss";

4. To add the Buckeye Interactive logo to the bottom corner of every page, add the following code between the closing `</div>` tags for `.reveal` and `.slides` in templates/_index.html:

        <footer id="global-footer">
          <a href="http://www.buckeyeinteractive.com/" rel="external">
            <img src="bower_components/buckii-reveal-theme/assets/logo.png" alt="Presented by Buckeye Interactive" />
          </a>
        </footer>