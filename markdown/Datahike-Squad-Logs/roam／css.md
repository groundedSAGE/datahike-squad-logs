- From [[Roam-Collective]]
    - Conventions::
        - Nest code under examples
            - #Meta
                - ```css
```
        - Add note under a #[[Change Log]] header in your Daily Notes Section, referencing the code block and detailing the change
        - Try to use the standard set of colors & variables as much as possible!
    - Shortcuts::
        - [Colors](((XIc8JmRnT)))
        - [Tag Styling](((k1T67c8R_)))
        - [Headings](((yPFdaV2UO)))
    - **Settings & Variables:**
        - Colors
            - Color Scheme
                - > Use names for consistent colors throughout your them —
                - Colors
                    - Black, White, Gray
                        - ```css
:root {
  --cl-white:    #ffffff;
  --cl-gray-100: #f8f9faff; /*--cultured*/
  --cl-gray-200: #e9ecefff; /*--cultured-2*/
  --cl-gray-300: #dee2e6ff; /*--gainsboro*/
  --cl-gray-400: #ced4daff; /*--light-gray*/
  --cl-gray-500: #adb5bdff; /*--cadet-blue-crayola*/
  --cl-gray-600: #6c757dff; /*--slate-gray*/
  --cl-gray-700: #495057ff; /*--davys-grey*/
  --cl-gray-800: #343a40ff; /*--gunmetal*/
  --cl-gray-900: #212529ff; /*--charleston-green*/
  --cl-black:    #000000;
}```

                    - Red
                        - ```css
:root {
  --cl-red-100: #ffc2c4ff; /*--spanish-pink*/
  --cl-red-200: #f9acafff; /*--light-pink*/
  --cl-red-300: #f3969aff; /*--salmon-pink*/
  --cl-red-400: #ed8084ff; /*--light-coral*/
  --cl-red-500: #e86b6fff; /*--candy-pink*/
  --cl-red-600: #e2555aff; /*--indian-red*/
  --cl-red-700: #dc3f45ff; /*--rose-madder*/
  --cl-red-800: #d6292fff; /*--amaranth-red*/
  --cl-red-900: #d0131aff; /*--lava*/
}```
                        - 

                    - Orange
                        - ```css
:root {
  --cl-orange-100: #ffcdadff; /*--apricot:*/
  --cl-orange-200: #fbbe97ff; /*--peach-crayola:*/
  --cl-orange-300: #f7af82ff; /*--macaroni-and-cheese:*/
  --cl-orange-400: #f3a06cff; /*--atomic-tangerine:*/
  --cl-orange-500: #f09257ff; /*--atomic-tangerine-2:*/
  --cl-orange-600: #ec8341ff; /*--princeton-orange:*/
  --cl-orange-700: #e8742bff; /*--spanish-orange:*/
  --cl-orange-800: #e46516ff; /*--spanish-orange-2:*/
  --cl-orange-900: #e05600ff; /*--persimmon:*/
}```

                    - Yellow
                        - ```css
:root {
  --cl-yellow-100: #FDEAB4ff; /*--jasmine:*/
  --cl-yellow-200: #fbdc86ff; /*--jasmine-2:*/
  --cl-yellow-300: #f7d473ff; /*--orange-yellow-crayola:*/
  --cl-yellow-400: #f3cc60ff; /*--maize-crayola:*/
  --cl-yellow-500: #f0c54dff; /*--maize-crayola-2:*/
  --cl-yellow-600: #ecbd39ff; /*--saffron:*/
  --cl-yellow-700: #e8b526ff; /*--orange-yellow:*/
  --cl-yellow-800: #e4ad13ff; /*--goldenrod:*/
  --cl-yellow-900: #e0a500ff; /*--goldenrod-2:*/

}```
                    - Green Yellow
                        - ```css
:root {
  --cl-green-yel-100: #eaecacff;/*--pale-spring-bud:*/
  --cl-green-yel-200: #e1e39bff;/*--green-yellow-crayola:*/
  --cl-green-yel-300: #d8da8bff;/*--khaki-x-11-light-khaki:*/
  --cl-green-yel-400: #cfd17aff;/*--straw:*/
  --cl-green-yel-500: #c6c96aff;/*--dark-khaki:*/
  --cl-green-yel-600: #bcc059ff;/*--olive-green:*/
  --cl-green-yel-700: #b3b748ff;/*--olive-green-2:*/
  --cl-green-yel-800: #aaae38ff;/*--citron:*/
  --cl-green-yel-900: #a1a527ff;/*--citron-2:*/
}```
                    - Green
                        - ```css
:root {
  --cl-green-100: #cae4a0ff; /*--yellow-green-crayola:*/
  --cl-green-200: #bed991ff; /*--yellow-green-crayola-2:*/
  --cl-green-300: #b2cf82ff; /*--pistachio:*/
  --cl-green-400: #a5c473ff; /*--olivine:*/
  --cl-green-500: #99ba64ff; /*--olivine-2:*/
  --cl-green-600: #8daf55ff; /*--olivine-3:*/
  --cl-green-700: #81a446ff; /*--moss-green:*/
  --cl-green-800: #749a37ff; /*--olive-drab-3:*/
  --cl-green-900: #688f28ff; /*--olive-drab-3-2:*/
}```
                    - Green-Blue
                        - ```css
:root {
  --cl-green-blu-100: #a8dcd9ff;/*--powder-blue:*/ 
  --cl-green-blu-200: #9ad3d0ff;/*--middle-blue-green:*/ 
  --cl-green-blu-300: #8dc9c6ff;/*--middle-blue-green-2:*/ 
  --cl-green-blu-400: #7fc0bdff;/*--green-sheen:*/ 
  --cl-green-blu-500: #72b7b3ff;/*--green-sheen-2:*/ 
  --cl-green-blu-600: #64adaaff;/*--verdigris:*/ 
  --cl-green-blu-700: #56a4a0ff;/*--cadet-blue:*/ 
  --cl-green-blu-800: #499a97ff;/*--cadet-blue-2:*/ 
  --cl-green-blu-900: #3b918dff;/*--viridian-green:*/ 
}```
                    - Blue (lighter shade)
                        - ```css
:root {
  --cl-blue-lt-100: #aec7efff; /*--baby-blue-eyes:*/
  --cl-blue-lt-200: #a0bce9ff; /*--baby-blue-eyes-2:*/
  --cl-blue-lt-300: #8fafe2ff; /*--french-sky-blue:*/
  --cl-blue-lt-400: #7ea5e0ff; /*--little-boy-blue:*/
  --cl-blue-lt-500: #7099daff; /*--cornflower-blue:*/
  --cl-blue-lt-600: #5f8cd3ff; /*--united-nations-blue:*/
  --cl-blue-lt-700: #4c7eceff; /*--glaucous:*/
  --cl-blue-lt-800: #3770cbff; /*--celtic-blue:*/
  --cl-blue-lt-900: #2b66c4ff; /*--true-blue:*/}```
                    - Blue
                        - ```css
:root {
  --cl-blue-100:   #dceff9ff; /*--alice-blue:*/
  --cl-blue-200:   #a7d9f1ff; /*--uranian-blue:*/
  --cl-blue-300:   #85c6e9ff; /*--light-cornflower-blue:*/
  --cl-blue-400:   #5aaddcff; /*--blue-jeans:*/
  --cl-blue-500:   #389bd5ff; /*--carolina-blue:*/
  --cl-blue-600:   #1e7ac0ff; /*--star-command-blue:*/
  --cl-blue-700:   #0254a0ff; /*--usafa-blue:*/
  --cl-blue-800:   #014889ff; /*--yale-blue:*/
  --cl-blue-900:   #023a72ff; /*--indigo-dye:*/
}```
                    - Blue (Darker Shade)
                        - ```css
:root {
  --cl-blue-dk-100: #7a8fd8ff; /* --cornflower-blue:  */
  --cl-blue-dk-200: #6e85d0ff; /* --glaucous:  */
  --cl-blue-dk-300: #6076c9ff; /* --han-blue:  */
  --cl-blue-dk-400: #526cc1ff; /* --han-blue-2:  */
  --cl-blue-dk-500: #455eb9ff; /* --liberty:  */
  --cl-blue-dk-600: #3f56aaff; /* --cerulean-blue:  */
  --cl-blue-dk-700: #3a4f99ff; /* --y-in-mn-blue:  */
  --cl-blue-dk-800: #30448fff; /* --dark-cornflower-blue:  */
  --cl-blue-dk-900: #263a83ff; /* --dark-cornflower-blue-2:  */}```
                    - Violet
                        - ```css
:root {
  --cl-violet-100: #afb1d4ff; /*--wild-blue-yonder*/
  --cl-violet-200: #a2a4caff; /*--blue-bell*/
  --cl-violet-300: #9597c0ff; /*--blue-bell-2*/
  --cl-violet-400: #888ab6ff; /*--cool-grey*/
  --cl-violet-500: #7b7eadff; /*--rhythm*/
  --cl-violet-600: #6e71a3ff; /*--dark-blue-gray*/
  --cl-violet-700: #616499ff; /*--dark-blue-gray-2*/
  --cl-violet-800: #54578fff; /*--purple-navy*/
  --cl-violet-900: #474a85ff; /*--purple-navy-2*/
}```
                    - Purple
                        - ```css
:root {
  --cl-purple-100: #bfaed5ff; /*--lilac*/
  --cl-purple-200: #b3a1cbff; /*--glossy-grape*/
  --cl-purple-300: #a894c2ff; /*--glossy-grape-2*/
  --cl-purple-400: #9c87b8ff; /*--purple-mountain-majesty*/
  --cl-purple-500: #907aaeff; /*--purple-mountain-majesty-2*/
  --cl-purple-600: #846ca4ff; /*--middle-blue-purple*/
  --cl-purple-700: #795f9bff; /*--royal-purple*/
  --cl-purple-800: #6d5291ff; /*--royal-purple-2*/
  --cl-purple-900: #614587ff; /*--cyber-grape*/
}```
                - Additional Color Schemes
                    - Togetic
                        - css
:root {
/*Togetic #176*/
  --cl-togetic-gray-500:  #737b83;
  --cl-togetic-gray-300:  #acc5bd;
  --cl-togetic-gray-100:  #d5eeee;
  --cl-togetic-red-500:   #bd1808;
  --cl-togetic-red-300:   #de4139;
  --cl-togetic-blue-500:  #1062bd;
  --cl-togetic-blue-300:  #2994e6;
}
                    - Wobbufet
                        - css
:root {
  /* CSS HEX */
  --uranian-blue: #a4deffff;
  --aero: #73bdf6ff;
  --blue-jeans: #52aceeff;
  --yale-blue: #20528bff;
  --gray-web: #838383ff;
  --davys-grey: #525252ff;
  --dark-orange: #ff8b00ff;
  --persimmon: #de5200ff;
  --rufous: #a41000ff;
}
            - Color Settings #Status/Inactive
                - UI
                    - All Pages
                        - > Modifies the "All Pages" site, found in the left sidebar
                        - Colors
                            - css
:root {
  --fg-all-pages-title:					var(--cl-gray-800);
  --bg-all-pages-header:				var(--cl-gray-100);
  --fg-all-pages-header:				var(--cl-gray-800);
  --fg-all-pages-header-sorted:			var(--cl-gray-900);
  --bg-all-pages-clickable-pill:		var(--cl-gray-800);
  --bg-all-pages-search:				var(--cl-white);
  --fg-all-pages-search:				var(--cl-gray-500);
  --fg-all-pages-search-placeholder:	var(--cl-gray-500);
  --fg-all-pages-title-col:				var(--cl-gray-500);
  --fg-all-pages-row:					var(--cl-gray-500);
  --br-all-pages-row:					var(--cl-gray-400);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-all-pages-title:					var(--cl-gray-800);
  --bg-all-pages-header:				var(--cl-gray-100);
  --fg-all-pages-header:				var(--cl-gray-800);
  --fg-all-pages-header-sorted:			var(--cl-gray-900);
  --bg-all-pages-clickable-pill:		var(--cl-gray-800);
  --bg-all-pages-search:				var(--cl-white);
  --fg-all-pages-search:				var(--cl-gray-500);
  --fg-all-pages-search-placeholder:	var(--cl-gray-500);
  --fg-all-pages-title-col:				var(--cl-gray-500);
  --fg-all-pages-row:					var(--cl-gray-500);
  --br-all-pages-row:					var(--cl-gray-400);  
  } 
}
                    - Brackets
                        - > Modifies the color of the Brackets when linking Pages
                        - Colors
                            - css
:root {
  --fg-brackets: var(--cl-gray-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
    --fg-brackets: var(--cl-gray-500);
  } 
}
                    - Buttons and Icons
                        - > Modifies icons in the top- and sidebar as well as buttons in the filter dialog.
                        - Colors
                            - css
:root {
  --fg-buttons:			var(--cl-gray-400);
  --bg-buttons: 		transparent;
  --fg-buttons-hover:	var(--cl-gray-500);
  --bg-buttons-hover:	transparent;
  --bg-word-count:		var(--cl-gray-100);
  --fg-word-count:		var(--cl-gray-700);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-buttons:			var(--cl-gray-400);
  --bg-buttons: 		transparent;
  --fg-buttons-hover:	var(--cl-gray-500);
  --bg-buttons-hover:	transparent;
  --bg-word-count:		var(--cl-gray-700);
  --fg-word-count:		var(--cl-gray-100);
  } 
}
                    - Caret
                        - > Modifies the little caret the folds bullets
                        - Colors
                            - css
:root {
  --fg-caret: 	var(--cl-gray-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-caret: 	var(--cl-gray-300);
  } 
}
                    - Help
                        - > Modifies the help dialog
                        - Colors
                            - css
:root {
  --bg-help:	var(--cl-gray-100);
  --fg-help:	var(--cl-gray-600);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-help:	var(--cl-gray-800);
  --fg-help:	var(--cl-gray-400);
  } 
}
                    - Left Sidebar
                        - > Modifies the left sidebar
                        - Colors
                            - css
:root {
  --bg-left-sidebar:		var(--cl-gray-50);
  --bg-left-sidebar-hover:	var(--cl-gray-50);
  --bg-left-sidebar-hr:		var(--cl-gray-500);
  --fg-left-sidebar:		var(--cl-gray-700);
  --fg-left-sidebar-hover:	var(--cl-gray-700);
  --fg-left-dropdown-title:	var(--cl-gray-400);
  --fg-left-sidebar-icons: 	var(--cl-gray-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-left-sidebar:		var(--cl-gray-800);
  --bg-left-sidebar-hover:	var(--cl-gray-800);
  --bg-left-sidebar-hr:		var(--cl-gray-500);
  --fg-left-sidebar:		var(--cl-gray-100);
  --fg-left-sidebar-hover:	var(--cl-white);
  --fg-left-dropdown-title:	var(--cl-gray-400);
  --fg-left-sidebar-icons: 	var(--cl-gray-400); 
  } 
}
                    - Log
                        - > Modifies the color of the daily log
                        - Colors
                            - css
:root {
  --fg-log-hr: 	var(--cl-gray-400);
  --fg-log:		var(--cl-gray-400);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-log-hr: 	var(--cl-gray-600);
  --fg-log:		var(--cl-gray-600);
  } 
}
                    - Menus
                        - > Changes the color and fonts of the different menus

**Notice**
We can't change the selection background in some menus yet, so make sure, that your colors will fit - avoid too light and too dark shades.
                        - Colors
                            - css
:root {
  --bg-menu:		var(--cl-white);
  --bg-menu-hover:	var(--cl-gray-100);
  --fg-menu:		var(--cl-gray-500);
  --fg-menu-hover:	var(--cl-gray-600);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-menu:		var(--cl-gray-800);
  --bg-menu-hover:	var(--cl-gray-200);
  --fg-menu:		var(--cl-gray-500);
  --fg-menu-hover:	var(--cl-gray-500);
  } 
}
                    - Top Bar
                        - > Modifies colors and fonts of the topbar including the  "Find or Create Page"-Input.
                        - Colors
                            - css
:root {
  --bg-topbar: 				var(--cl-white);
  --bg-input: 				var(--cl-gray-50);
  --br-input: 				var(--cl-gray-100);
  --fg-input: 				var(--cl-gray-800);
  --fg-input-placeholder: 	var(--cl-gray-400);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-topbar: 				var(--cl-gray-900);
  --bg-input: 				var(--cl-gray-800);
  --br-input: 				var(--cl-gray-700);
  --fg-input: 				var(--cl-gray-100);
  --fg-input-placeholder: 	var(--cl-gray-400);
  } 
}
                    - In-Line References
                        - css
:root {
	--bg-inline-refs: 	var(--cl-gray-50);
}

@media (prefers-color-scheme: dark) {
  :root { 
	--bg-inline-refs: 	var(--cl-gray-600);
  } 
}
                - Content
                    - Body
                        - css
:root {
  --primary-color: 		var(--cl-gray-800);
  --background-color: 	var(--cl-white);
  --bg-body:			var(--cl-white);
  --fg-body:			var(--cl-gray-800);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --primary-color: 		var(--cl-blue-500);
  --background-color: 	var(--cl-gray-900);
  --bg-body:			var(--cl-gray-900);
  --fg-body:			var(--cl-gray-50);

  } 
}
                    - Breadcrumbs
                        - > Modifies the breadcrumbs (zoom items)
                        - css
:root {
  --bg-zoom:			transparent;
  --fg-zoom:			var(--cl-gray-500);
  --bg-zoom-mask:		var(--cl-white);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-zoom:			transparent;
  --fg-zoom:			var(--cl-gray-500);
  --bg-zoom-mask:		var(--cl-gray-50);

  } 
}
                    - Bullets and Lines
                        - > Changes the bullets and lines for blocks
                        - Preview
                            - A single bullet
                                - A line to the left
                            - A closed bullet
                        - css
:root {
  --bg-bullet-inner:	var(--cl-gray-200);
  --br-bullet-outer:	var(--cl-gray-200);
  --br-block:			var(--cl-gray-200);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-bullet-inner:	var(--cl-gray-700);
  --br-bullet-outer:	var(--cl-gray-500);
  --br-block:			var(--cl-gray-600);
  } 
}
                    - Headings
                        - > Modifies the Headings Level 1 - 3
                        - Preview
                            - Heading 1
                                - Heading 2
                                    - Heading 3
                        - clojure
:root {
  --fg-h1:				var(--cl-gray-900);
  --fg-h2:				var(--cl-gray-900);
  --fg-h3:				var(--cl-gray-900);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-h1:				var(--cl-gray-50);
  --fg-h2:				var(--cl-gray-50);
  --fg-h3:				var(--cl-gray-50);
  } 
}
                    - Highlights
                        - > Modifies the highlights
                        - Preview
                            - ^^This text is highlighted^^
                        - Colors
                            - css
:root {
  --bg-highlight:		var(--cl-blue-50);
  --bg-highlight-blue:	var(--cl-blue-200);
  --bg-highlight-yellow:var(--cl-blue-200);
  --bg-highlight-grey:	var(--cl-gray-200);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-highlight:		var(--cl-beige-500);
  --bg-highlight-blue:	var(--cl-blue-500);
  --bg-highlight-yellow:var(--cl-blue-500);
  --bg-highlight-grey:	var(--cl-gray-500);
  } 
}
                    - Page Reference Links
                        - > Modifies the color of links and references pages
                        - Preview
                            - This is [a link](http://link.com), this is a reference to a page [[Test Page]], this is a [[Project/Complete Job Search & Get Hired]] namespace, this is a double underline [[Podcasts/Remote Work (podcasts)]]
                        - Colors
                            - css
:root {
  --fg-link:						var(--cl-green-500);
  --fg-link-hover:					var(--cl-green-500);
  --fg-reference:					var(--cl-togetic-blue-500);
  --fg-reference-hover:				var(--cl-togetic-blue-300);
  --fg-namespace:					var(--cl-togetic-red-300);
  --fg-namespace-hover:				var(--cl-togetic-red-500);
  --fg-reference-underline:			var(--cl-togetic-gray-300);
  --fg-reference-underline-hover:	var(--cl-togetic-blue-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-link:						var(--cl-togetic-blue-300);
  --fg-link-hover:					var(--cl-blue-500);
  --fg-reference:					var(--cl-togetic-red-300);
  --fg-reference-hover:				var(--cl-togetic-red-500);
  --fg-namespace:					var(--cl-orange-500);
  --fg-namespace-hover:				var(--cl-orange-500); 
  --fg-reference-underline:			var(--cl-gray-300);
  --fg-reference-underline-hover:	var(--cl-orange-500);
  } 
}
                    - Block References
                        - > Modifies the background of the reference blocks
                        - Preview
                            - ((IeFN6yma5))
                        - Colors
                            - css
:root {
  --bg-reference:				var(--cl-gray-50);
  --bg-block-ref:				none;
  --bg-block-ref-hover: 		none;
  --fg-block-ref-underline:		var(--cl-gray-100);
  --fg-block-ref-start:			var(--cl-orange-500);
  --fg-block-ref-end:			var(--cl-indigo-500);
}

@media (prefers-color-scheme: dark) {
  :root {
  --bg-reference:				var(--cl-gray-800);
  --bg-block-ref:				none;
  --bg-block-ref-hover: 		none;
  --fg-block-ref-underline:		var(--cl-gray-100);
  --fg-block-ref-start:			var(--cl-orange-500);
  --fg-block-ref-end:			var(--cl-gray-50);
  }
}
                    - Tags
                        - > Modifies the apperance of tags
                        - Preview
                            - #tag1 #tag2
                        - Colors
                            - css
:root {
  --fg-tag:				var(--cl-gray-500);
  --bg-tag:				none;
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-tag:				var(--cl-gray-500);
  --bg-tag:				none;
  } 
}
                - Special Blocks
                    - Calc
                        - > Modifies the color of the calculation result
                        - Preview
                            - {{[[calc]]: 31 + 11}}
                        - Colors
                            - css
:root {
  --fg-calc:		var(--cl-green-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-calc:		var(--cl-green-500);
  } 
}
                    - Code
                        - > Modifies the color of Codeblocks and Inline Code
                        - Preview
                            -  and Codeblocks:
                                - javascript
const baseValue = prompt('Enter the base of a triangle: ');
const heightValue = prompt('Enter the height of a triangle: ');

// calculate the area
const areaValue = (baseValue * heightValue) / 2;

console.log(
  `The area of the triangle is ${areaValue}`
);
                        - Inline Code
                            - Colors
                                - css
:root {
  --fg-inline-code:			var(--cl-gray-800);
  --bg-inline-code:			var(--cl-gray-50);
  --br-inline-code:			var(--cl-gray-50);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --fg-inline-code:			var(--cl-gray-50);
  --bg-inline-code:			var(--cl-gray-700);
  --br-inline-code:			var(--cl-gray-700);  
  } 
}
                        - Code Block
                            - Colors - Light
                                - css
:root {
  --bg-code:						var(--cl-gray-50);
  --bg-code-filler:					var(--cl-gray-50);
  --bg-code-gutters:				var(--cl-gray-50);
  --bg-code-selected:				var(--cl-gray-300);
  --bg-code-selection:				var(--cl-blue-200);
  --bg-code-focused:				var(--cl-blue-200);
  --bg-code-searching:				rgba(255, 255, 0, 0.4);	
  --bg-code-matchingtag:			rgba(255, 150, 0, 0.3);
  --bg-code-activeline:				var(--cl-white);
  --bg-code-fat-cursor:				#7e7;
  --bg-code-fat-cursor-mark:		rgba(20, 255, 20, 0.5);
  --bg-code-fat-cursor-animate:		#7e7;
  --br-code-gutters:				var(--cl-gray-100);
  --br-code-cursor:					var(--cl-black);
  --br-code-secondary-cursor:		var(--cl-gray-400);
  --br-code-ruler:					var(--cl-gray-400);
  --fg-code-linenumber:				var(--cl-gray-500);
  --fg-code-guttermarker:			var(--cl-black);
  --fg-code-guttermarker-subtle: 	var(--cl-gray-500);
}
                            - Colors - Dark
                                - css
@media (prefers-color-scheme: dark) {
  :root { 
  --bg-code:						var(--cl-gray-800);
  --bg-code-filler:					var(--cl-gray-800);
  --bg-code-gutters:				var(--cl-gray-800);
  --bg-code-selected:				var(--cl-gray-300);
  --bg-code-selection:				var(--cl-blue-200);
  --bg-code-focused:				var(--cl-blue-200);
  --bg-code-searching:				rgba(255, 255, 0, 0.4);	
  --bg-code-matchingtag:			rgba(255, 150, 0, 0.3);
  --bg-code-activeline:				var(--cl-white);
  --bg-code-fat-cursor:				#7e7;
  --bg-code-fat-cursor-mark:		rgba(20, 255, 20, 0.5);
  --bg-code-fat-cursor-animate:		#7e7;
  --br-code-gutters:				var(--cl-gray-900);
  --br-code-cursor:					var(--cl-white);
  --br-code-secondary-cursor:		var(--cl-gray-600);
  --br-code-ruler:					var(--cl-gray-600);
  --fg-code-linenumber:				var(--cl-gray-500);
  --fg-code-guttermarker:			var(--cl-black);
  --fg-code-guttermarker-subtle: 	var(--cl-gray-500);
  } 
}
                        - Syntax Highlighting
                            - Colors - Light
                                - css
:root {  
  --fg-code:					var(--cl-gray-400);
  --fg-code-header:				var(--cl-blue-500);
  --fg-code-quote:				var(--cl-green-500);
  --fg-code-negative:			var(--cl-green-500);
  --fg-code-positive:			var(--cl-green-500);
  --fg-code-keyword:			var(--cl-purple-500);
  --fg-code-atom:				var(--cl-blue-500);
  --fg-code-number:				var(--cl-green-500);
  --fg-code-def:				var(--cl-blue-500);
  --fg-code-variable-2:			var(--cl-indigo-500);
  --fg-code-variable-3:			var(--cl-green-500);
  --fg-code-comment:			var(--cl-brown-500);
  --fg-code-string:				var(--cl-green-500);
  --fg-code-string-2:			var(--cl-orange-500);
  --fg-code-meta:				var(--cl-gray-400);
  --fg-code-qualifier:			var(--cl-gray-400);
  --fg-code-builtin:			var(--cl-indigo-500);
  --fg-code-bracket:			var(--cl-gray-500);
  --fg-code-tag:				var(--cl-green-500);
  --fg-code-attribute:			var(--cl-blue-500);
  --fg-code-hr:					var(--cl-gray-600);
  --fg-code-link:				var(--cl-blue-500);
  --fg-code-error:				var(--cl-green-500);
  --fg-code-invalidchar:		var(--cl-green-500);
  --fg-code-matchingbracket: 	var(--cl-green-500);
  --fg-code-nonmatchingbracket:	var(--cl-green-500);
}
                            - Colors - Dark
                                - css
@media (prefers-color-scheme: dark) {
  :root { 
  --fg-code:					var(--cl-gray-300);
  --fg-code-header:				var(--cl-blue-500);
  --fg-code-quote:				var(--cl-green-500);
  --fg-code-negative:			var(--cl-green-500);
  --fg-code-positive:			var(--cl-green-500);
  --fg-code-keyword:			var(--cl-purple-500);
  --fg-code-atom:				var(--cl-blue-500);
  --fg-code-number:				var(--cl-green-500);
  --fg-code-def:				var(--cl-blue-500);
  --fg-code-variable-2:			var(--cl-indigo-500);
  --fg-code-variable-3:			var(--cl-green-500);
  --fg-code-comment:			var(--cl-brown-500);
  --fg-code-string:				var(--cl-green-500);
  --fg-code-string-2:			var(--cl-orange-500);
  --fg-code-meta:				var(--cl-gray-400);
  --fg-code-qualifier:			var(--cl-gray-400);
  --fg-code-builtin:			var(--cl-indigo-500);
  --fg-code-bracket:			var(--cl-gray-500);
  --fg-code-tag:				var(--cl-green-500);
  --fg-code-attribute:			var(--cl-blue-500);
  --fg-code-hr:					var(--cl-gray-600);
  --fg-code-link:				var(--cl-blue-500);
  --fg-code-error:				var(--cl-green-500);
  --fg-code-invalidchar:		var(--cl-green-500);
  --fg-code-matchingbracket: 	var(--cl-green-500);
  --fg-code-nonmatchingbracket:	var(--cl-green-500);  
  } 
}
                    - Diagrams
                        - > Diagrams can't be modified yet. This is a problem with dark mode settings.
                        - Preview
                            - {{[[diagram]]}}
                                - A
                                - B
                    - Embed
                        - > Changes the background color of embed blocks
                        - Preview
                            - Sample Data
                                - Embed 1
                                    - {{[[embed]]: ((ZuyIjM6mE))}}
                                - Embed 2
                                    - {{[[embed]]: ((oVEJn3mnp))}}
                                - Embed 3
                            - {{[[embed]]: ((CR-dOUiRZ))}}
                        - Colors
                            - css
:root {
  --bg-embed-1: 	var(--cl-gray-50);
  --bg-embed-2: 	var(--cl-gray-100);
  --bg-embed-3: 	var(--cl-gray-200);
  --bg-embed-4: 	var(--cl-gray-300);
  --bg-embed-5: 	var(--cl-gray-400);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-embed-1: 	var(--cl-gray-800);
  --bg-embed-2: 	var(--cl-gray-700);
  --bg-embed-3: 	var(--cl-gray-600);
  --bg-embed-4: 	var(--cl-gray-500);
  --bg-embed-5: 	var(--cl-gray-400);  
  } 
}
                    - HR
                        - > Modifies horizontal lines
                        - Preview
                            - ---
                        - Colors
                            - css
:root {
 --br-hr:	var(--cl-gray-300);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --br-hr:	var(--cl-gray-300);
  } 
}
                    - Kanban
                        - > Modifies Kanban boards
                        - Preview
                            - {{[[kanban]]}}
                                - Ready
                                    - Card 1
                                - Done
                                    - Card 2
                        - Colors
                            - css
:root {
  --bg-kanban-board: 	var(--cl-gray-50);
  --br-kanban-board:	var(--cl-white);
  --bg-kanban-column:	var(--cl-gray-100);
  --bg-kanban-card:		var(--cl-white);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-kanban-board: 	var(--cl-gray-800);
  --br-kanban-board:	var(--cl-black);
  --bg-kanban-column:	var(--cl-gray-900);
  --bg-kanban-card:		var(--cl-black);  
  } 
}
                    - Mermaid
                        - > Modifies Mermaid diagrams
                        - Preview
                            - {{mermaid}}
                                - graph TD;
                                    - A-->B;
                                    - A-->D;
                                    - B-->D;
                                    - C-->D;
                        - Colors
                            - css
:root {
  --bg-mermaid: 		var(--cl-white);
  --bg-mermaid-node: 	var(--cl-gray-300);
  --fg-mermaid-label: 	var(--cl-gray-800);
  --br-mermaid-node: 	var(--cl-gray-500);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-mermaid: 		var(--cl-white);
  --bg-mermaid-node: 	var(--cl-gray-300);
  --fg-mermaid-label: 	var(--cl-gray-800);
  --br-mermaid-node: 	var(--cl-gray-500);  
  } 
}
                    - Queries
                        - > Modifies the appearance of queries
                        - Preview
                            - {{[[query]]: {and: [[TODO]] [[December 30th, 2020]]}}}
                        - Colors
                            - css
:root {
  --bg-query-title:		var(--cl-gray-100);
  --fg-query-title:		var(--cl-gray-600);
  --br-query:			var(--cl-gray-200);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-query-title:		var(--cl-gray-900);
  --fg-query-title:		var(--cl-gray-400);
  --br-query:			var(--cl-gray-700);  
  } 
}
                    - Quote
                        - > Modifies the design of quotes
                        - Preview
                            - > This is a famous quote!
                        - Color
                            - css
:root {
  --bg-quote:			var(--cl-white);
  --br-quote:			var(--cl-gray-800);
  --fg-quote:			var(--cl-gray-800);  
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-quote:			var(--cl-gray-900);
  --br-quote:			var(--cl-gray-500);
  --fg-quote:			var(--cl-gray-100);    
  } 
}
                    - Tables
                        - > Modifies tables
                        - Preview
                            - {{[[table]]}}
                                - Column 1
                                    - Column 2
                                - Row 1
                                    - Row 2
                        - Colors
                            - css
:root {
  --br-table:	var(--cl-gray-300);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --br-table:	var(--cl-gray-600);
  } 
}
                    - Todo
                        - > Modifies the design of todos
                        - Preview
                            - {{[[TODO]]}} This is a todo
                            - {{[[DONE]]}} This is a finished todo
                        - Colors
                            - css
:root {
  --br-checkbox: var(--cl-gray-300);
  --bg-checkbox-checked: var(--cl-gray-300);
  --br-checkmark: var(--cl-white);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --br-checkbox: var(--cl-gray-600);
  --bg-checkbox-checked: var(--cl-gray-600);
  --br-checkmark: var(--cl-white);  
  } 
}
                    - Versions
                        - > Modifies the design of the version block
                        - Preview
                            - Version 2
                        - Colors
                            - css
:root {
  --bg-version-bullet: 		var(--cl-gray-400);
  --fg-version-selected: 	var(--cl-blue-500);
  --br-version:				var(--cl-gray-300);
}

@media (prefers-color-scheme: dark) {
  :root { 
  --bg-version-bullet: 		var(--cl-gray-600);
  --fg-version-selected: 	var(--cl-blue-500);
  --br-version:				var(--cl-gray-600);  
  } 
}
                - Custom
                    - css
:root {
  --note-tag-color:				var(--cl-gray-700);
}

@media (prefers-color-scheme: dark) {
  :root {
  	--note-tag-color:			var(--cl-gray-200);
  }
}
        - Fonts
            - Code Blocks
                - Code
                    - ```css
:root {
  --fnt-size-inline-code:		12px;
  --fnt-size-code-block:		14px;
}

.CodeMirror .CodeMirror-code pre {
  font-size: var(--fnt-size-code-block);
  font-style: normal!important;
}

code {
  font-size: var(--fnt-size-inline-code);
  font-style: normal!important;
}```

                    - Example: `this is a code block`
    - Code::
        - Elements
            - Tags
                1. Variables
                    - ```css
:root {
  /*
  Format:
  --tag-bg-cl-<family-name>: 	var(--cl-<color-name>);
  */
  --tag-bg-cl-gtd:		var(--cl-blue-500);
}```
                2. Top-Section Tags
                    - #[[Community Notes]] [[Roam Collective]]
                        - ```css
span.rm-page-ref[data-tag="Community Notes"] {
	background-image: linear-gradient(to right, var(--cl-gray-800),var(--cl-gray-800));
	background-size: 100%;
    color: var(--cl-white);
    padding: 3px 2px 3px 5px;
    font-size: 13px;
    line-height: 1em;
    border-radius: 3px 0 0 3px;
    position:relative;
}

 span.rm-page-ref[data-tag="Community Notes"] + span[data-link-title] {
     background: var(--cl-gray-400) !important;
     color: var(--cl-gray-900) !important;
     padding: 3px 5px 3px 15px;
     font-size: 13px;
     line-height: 1em;
     font-weight: 400;
     border-radius: 0 3px 3px 0;
     margin-left: -5px;
}


span.rm-page-ref[data-tag="Community Notes"]:after, span.rm-page-ref[data-tag="Post"]:before {
    left: 100%;
    top: 50%;
    border: solid transparent;
    content: " ";
    height: 0;
    width: 0;
    position: absolute;
    pointer-events: none;
}

span.rm-page-ref[data-tag="Community Notes"]:after {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-800);
    border-width: 11px;
    margin-top: -11px;
}

span.rm-page-ref[data-tag="Community Notes"]:before {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-800);
    border-width: 11px;
    margin-top: -11px;
}```
                    - #Announcements 
                        - ```css
span.rm-page-ref[data-tag="Announcements"] {
    background: #F44336;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Announcements"]:before {
    content: '📢'
}```
                    - #[[Daily Log]]
                        - ```css
span.rm-page-ref[data-tag="Daily Log"] {
    background: #FF9800;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Daily Log"]:before {
    content: '📆'
}```
                    - #[[Chat]]
                        - ```css
span.rm-page-ref[data-tag="Chat"] {
    background: var(--cl-blue-500);
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Chat"]:before {
    content: '📢'
}```
                    - #[[The Main Feed]]
                        - ```css
span.rm-page-ref[data-tag="The Main Feed"] {
	background: var(--cl-orange-600);
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="The Main Feed"]:before {
    content: '⭐️'
}```
                3. Squad Modules
                    - #[[Squad Logs]] [[Lead [[Your Name]]]]
                        - ```css
span.rm-page-ref[data-tag="Squad Logs"] {
	background-image: linear-gradient(to right, var(--cl-gray-800),var(--cl-gray-800));
	background-size: 100%;
    color: var(--cl-white);
    padding: 3px 2px 3px 5px;
    font-size: 13px;
    line-height: 1em;
    border-radius: 3px 0 0 3px;
    position:relative;
}

 span.rm-page-ref[data-tag="Squad Logs"] + span[data-link-title] {
     background: var(--cl-gray-400) !important;
     color: var(--cl-gray-900) !important;
     padding: 3px 5px 3px 15px;
     font-size: 13px;
     line-height: 1em;
     font-weight: 400;
     border-radius: 0 3px 3px 0;
     margin-left: -5px;
}


span.rm-page-ref[data-tag="Squad Logs"]:after, span.rm-page-ref[data-tag="Post"]:before {
    left: 100%;
    top: 50%;
    border: solid transparent;
    content: " ";
    height: 0;
    width: 0;
    position: absolute;
    pointer-events: none;
}

span.rm-page-ref[data-tag="Squad Logs"]:after {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-800);
    border-width: 11px;
    margin-top: -11px;
}

span.rm-page-ref[data-tag="Squad Logs"]:before {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-800);
    border-width: 11px;
    margin-top: -11px;
}```
                4. DNP Modules
                    - #[[My Daily Notes]] [[Your Name]]
                        - ```css
span.rm-page-ref[data-tag="My Daily Notes"] {
	background-image: linear-gradient(to right, var(--cl-gray-600),var(--cl-gray-600));
	background-size: 100%;
    color: var(--cl-white);
    padding: 3px 2px 3px 5px;
    font-size: 13px;
    line-height: 1em;
    border-radius: 3px 0 0 3px;
    position:relative;
}

 span.rm-page-ref[data-tag="My Daily Notes"] + span[data-link-title] {
     background: var(--cl-gray-200) !important;
     color: var(--cl-gray-900) !important;
     padding: 3px 5px 3px 15px;
     font-size: 13px;
     line-height: 1em;
     font-weight: 400;
     border-radius: 0 3px 3px 0;
     margin-left: -5px;
}


span.rm-page-ref[data-tag="My Daily Notes"]:after, span.rm-page-ref[data-tag="Post"]:before {
    left: 100%;
    top: 50%;
    border: solid transparent;
    content: " ";
    height: 0;
    width: 0;
    position: absolute;
    pointer-events: none;
}

span.rm-page-ref[data-tag="My Daily Notes"]:after {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-600);
    border-width: 11px;
    margin-top: -11px;
}

span.rm-page-ref[data-tag="My Daily Notes"]:before {
    border-color: rgba(255,255,255,0);
    border-left-color: var(--cl-gray-600);
    border-width: 11px;
    margin-top: -11px;
}```
                    - #[[Scratchpad]]
                        - ```css
span.rm-page-ref[data-tag="Scratchpad"] {
    background: var(--cl-yellow-800);
    color: var(--cl-white);
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Scratchpad"]:before {
    content: '✏️';
}```
                    - #Conversation
                        - ```css
span.rm-page-ref[data-tag="Conversation"] {
    background: var(--cl-green-700);
    color: var(--cl-white);
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Conversation"]:before {
    content: '💬'
}```
                    - #[[Change Log]]
                        - ```css
span.rm-page-ref[data-tag="Change Log"] {
    background: var(--cl-gray-600);
    color: var(--cl-white);
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Change Log"]:before {
    content: '📢'
}```
                    - #Questions
                        - ```css
span.rm-page-ref[data-tag="Questions"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Questions"]:before {
    content: '❓'
}```
                    - "#[[Daily Log]]"
                    - #[[Help Wanted]]
                        - ```css
span.rm-page-ref[data-tag="Help Wanted"] {
    background: #9C27B0;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Help Wanted"]:before {
    content: '😃'
}```
                    - #[[Feedback & Questions]]
                        - ```css
span.rm-page-ref[data-tag="Feedback & Questions"] {
    background: var(--cl-purple-900);
    color: var(--cl-white);
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Feedback & Questions"]:before {
    content: '📢';
}```
                    - #Chat
                    - #Bookmarks
                        - ```css
span.rm-page-ref[data-tag="Bookmarks"] {
    background: var(--cl-blue-500);
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Bookmarks"]:before {
    content: '💾';
}```
                5. Notifications & Mentions
                    - [[@[[Their Name]]]]
                        - ```css
span[data-link-title^="@"] {
        border: 2px solid #B35555 !important;
        padding: 3px 6px 3px 7px;
        margin-right: 1px;
    	line-height: 2em;
} 

span[data-link-title^="@"]:before {
    color: #000746 !important;
    content: "🚨unread ";
}

span[data-link-title^="@[[Everyone]]"]:before {
    color: #000746 !important;
    content: "🚨🚨" !important;
}```
                    - [[cc:[[Their Name]]]]
                        - ```css
span[data-link-title^="cc:"] {
        border: 2px solid #2196F3 !important;
        padding: 3px 6px 3px 7px;
        margin-right: 1px;
    line-height: 2em;
} 

span[data-link-title^="cc:"]:before {
    color: #000746 !important;
    content: "📨 ";
}```
                    - [[~[[Your Name]]]]
                        - ```css
span[data-link-title^="~"] {
        border: 2px solid #02B920 !important;
        padding: 3px 6px 3px 7px;
        margin-right: 1px;
    	line-height: 2em;
} 

span[data-link-title^="~"]:before {
    color: #000746 !important;
    content: "✅read "
}```
                    - [[^[[Your Name]]]]
                        - ```css
span[data-link-title^="^"] {
        border: 2px solid #4CAF50 !important;
        padding: 3px 6px 3px 7px;
        margin-right: 1px;
    line-height: 2em;
} 

span[data-link-title^="^"]:before {
    color: #000746 !important;
    content: "💾saved "
}```
                6. Block-level Tags
                    - #[[I]] (Ideas)
                        - ```css
span.rm-page-ref[data-tag="I"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="I"]:before {
    content: '💡'
}```
                    - #Q (Questions)
                        - ```css
span.rm-page-ref[data-tag="Q"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Q"]:before {
    content: '❓'
}```
                    - #Ans (Answers)
                        - ```css
span.rm-page-ref[data-tag="Ans"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Ans"]:before {
    content: '✅'
}```
                        - css
span.rm-page-ref[data-tag="Ans"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Ans"]:before {
    content: '✅'
}
                    - #[[Obs]] (Observations)
                        - ```css
span.rm-page-ref[data-tag="Obs"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Obs"]:before {
    content: '👀'
}```
                    - #G (Goals)
                        - ```css
span.rm-page-ref[data-tag="G"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="G"]:before {
    content: '🏆'
}```
                7. Page-type Tags
                    - #People
                        - ```css
span.rm-page-ref[data-tag="People"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="People"]:before {
    content: '😃'
}```
                    - #Members
                        - ```css
span.rm-page-ref[data-tag="Members"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Members"]:before {
    content: '🔑'
}```
                    - #[[Meetings & Discussions]]
                        - ```css
span.rm-page-ref[data-tag="Meetings & Discussions"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Meetings & Discussions"]:before {
    content: '👥'
}```
                    - #[[Engineering & Building]]
                        - ```css
span.rm-page-ref[data-tag="Engineering & Building"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Engineering & Building"]:before {
    content: '🛠️'
 
}```
                    - #Podcasts
                        - ```css
span.rm-page-ref[data-tag="Podcasts"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Podcasts"]:before {
    content: '🎙'
}```
                    - #Tips
                        - ```css
span.rm-page-ref[data-tag="Tips"] {
    background: #9E9E9E;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Tips"]:before {
    content: '☝️'
}```
                8. GTD Tags
                    - Examples
                        - #[[GTD Zone]]
                        - #Agenda
                    - Code
                        - ```css
:root {
  --background: var(--cl-blue-lt-700);
  --color: var(--cl-white);
  --padding:2px 5px 2px 5px;
  --font-size: 13px;
  --line-height: 1em;
  --font-weight: 500;
  --border-radius: 5px 5px 5px 5px;
  --position:relative; 
}

span.rm-page-ref[data-tag="GTD Zone"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="GTD Zone"]:before {
    content: '✅';
}

span.rm-page-ref[data-tag="INBOX"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="INBOX"]:before {
    content: '📥'
}

span.rm-page-ref[data-tag="Inbox"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Inbox"]:before {
    content: '📥'
}

span.rm-page-ref[data-tag="Projects"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Projects"]:before {
    content: '🔨'
}

span.rm-page-ref[data-tag="Goals"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Goals"]:before {
    content: '🎯'
}

span.rm-page-ref[data-tag="Follow Up"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Follow Up"]:before {
    content: '📌'
}

span.rm-page-ref[data-tag="Agenda"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Agenda"]:before {
    content: '🗓'
}

span.rm-page-ref[data-tag="Mindsweep"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Mindsweep"]:before {
    content: '🧹'
}

span.rm-page-ref[data-tag="Waiting"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Waiting"]:before {
    content: '⏱'
}

span.rm-page-ref[data-tag="Waiting-[[resolved]]"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Waiting-[[resolved]]"]:before {
    content: '☑️'
}

span.rm-page-ref[data-tag="Tracking"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Tracking"]:before {
    content: '👀'
}

span.rm-page-ref[data-tag="Daily Big 3"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Daily Big 3"]:before {
    content: '🚩'
}

span.rm-page-ref[data-tag="Plan My Day"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Plan My Day"]:before {
    content: '🎯'
}

span.rm-page-ref[data-tag="Weekly Preview"] {
    background: var(--background);
    color: var(--color);
    padding: var(--padding);
    font-size: var(--font-size);
    line-height: var(--line-height);
    font-weight: var(--font-weight);
    border-radius: var(--border-radius);
    position: var(--position);
}

span.rm-page-ref[data-tag="Weekly Preview"]:before {
    content: '🗓'
}```
                9. Highlight Tags
                    - #Highlights
                        - ```css
span.rm-page-ref[data-tag="Highlights"] {
    background: #FFC107;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Highlights"]:before {
    content: ''
}```
                    - #[[My Wins]]
                        - ```css
span.rm-page-ref[data-tag="My Wins"] {
    background: #4CAF50;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="My Wins"]:before {
    content: '🏆'
}```
                    - #[[Our Wins]]
                        - ```css
span.rm-page-ref[data-tag="Our Wins"] {
    background: #4CAF50;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Our Wins"]:before {
    content: '🏆'
}```
                10. Journaling Tags
                    - #[[Today I Learned]]
                        - ```css
span.rm-page-ref[data-tag="Today I Learned"] {
    background: #9C27B0;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Today I Learned"]:before {
    content: '⚡️'
}```
                    - #[[Reflection]]
                        - ```css
span.rm-page-ref[data-tag="Reflection"] {
    background: #607D8B;
    color: #fff;
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Reflection"]:before {
    content: '💬'
}```
                11. Status Tags
                    - Root css
                        - ```css
:root {
  --status-padding: 1px 1px 1px 1px;
}```
                    - #Status/Enabled
                        - ```css
span.rm-page-ref[data-tag="Status/Enabled"] {
    color: #4CAF50;
    padding: var(--status-padding);
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}```
            - User Interface
                - Buttons & Word Count #Status/Enabled
                    - Example: {{word-count}}
                    - Code
                        - ```css
/* Buttons in Block Text */
.rm-block-text > span > .bp3-button:not([class*="bp3-intent-"]),
.rm-block-text > span > .bp3-button:not([class*="bp3-intent-"]):focus,
.rm-block-text > span > .bp3-button:not([class*="bp3-intent-"]):hover {
  background-color: #D1D1D1;
  font-size: 12px;
  line-height: 12px;
  padding: 2px 4px 2px 4px; 
  min-height: 0px;
}

/* Buttons in Block References */
	.rm-block-ref > span > .bp3-button:not([class*="bp3-intent-"]),
	.rm-block-ref > span > .bp3-button:not([class*="bp3-intent-"]):focus,
	.rm-block-ref > span > .bp3-button:not([class*="bp3-intent-"]):hover {
	background-color: #D1D1D1;
	font-size: 12px;
	line-height: 12px;
	padding: 2px 4px 2px 4px; 
	min-height: 0px;
}

/* Buttons in Zoom Masks */
	.rm-zoom-item > span > div > div > span > .bp3-button:not([class*="bp3-intent-"]),
	.rm-zoom-item > span > div > div > span > .bp3-button:not([class*="bp3-intent-"]):focus,
	.rm-zoom-item > span > div > div > span > .bp3-button:not([class*="bp3-intent-"]):hover {
	background-color: #D1D1D1;
	font-size: 12px;
	line-height: 12px;
	padding: 2px 4px 2px 4px; 
	min-height: 0px;
}```

                - Scope Highlighting ((This colors the vertical lines to show your mouse location and the bullet that you are editing)) #Status/Enabled
                    - ```css
.roam-block-container  div.roam-block-container {
box-shadow: -2px 0px var(--cl-gray-600));
transition: box-shadow 1s;
}

.roam-block-container div.roam-block-container:hover {
box-shadow: -0.5px 0px var(--cl-gray-800);
transition:  box-shadow 0.5s;
}

.roam-block-container:focus-within > .rm-block-main > div:nth-child(1) 
.rm-bullet .rm-bullet__inner  
{
background-color: var(--cl-black);
}```
                - Left Sidebar — Highlight important pages #Status/Enabled
                    - "[[Welcome 😃]]"
                    - ```css

.starred-pages a[href*="VP5hU0EoH"]>.page,
.starred-pages a[href*="1yilY3kHX"]>.page,
.starred-pages a[href*="ccmi5U8fX"]>.page,
.starred-pages a[href*="tcURDg2cN"]>.page
{
  color: #FFCF40 !important;
}

.starred-pages a[href*="cwZ9xV-cp"]>.page,
.starred-pages a[href*="jzJhiUFXk"]>.page,
.starred-pages a[href*="cXU68xJim"]>.page,
.starred-pages a[href*="8qmDeH08U"]>.page
{
  color: #2196F3 !important;
}

.starred-pages a[href*="Cxdcd0yBk"]>.page,
.starred-pages a[href*="XvU7pawsS"]>.page,
{
  color: #9E9E9E !important;
}```
                - Query Display Options #Status/Enabled
                    - ```css
/* RR change: MINIMIZE QUERIES: add any one of the following tags 
before the beginning of your query (in the same block):

    #min-title = hides the page reference link / page title
    #min-con = hides the contextual reference information (breadcrumbs)
    #minimal = hides both the title and the context
    #min-q = hides the query string, similar to legacy behavior
    #min-all = hides everything — title, context, and query string
	#page-focus = only displays pages

inspired by Matt Goldenberg */

[data-tag="minimal"], 
[data-tag="minimal"] + .rm-query .rm-title-arrow-wrapper,
[data-tag="minimal"] + .rm-query .zoom-mentions-view {
  display:none!important; /* hide page reference (title) and mention context (breadcrumbs) */
}

[data-tag="min-title"], [data-tag="min-title"] + .rm-query .rm-title-arrow-wrapper {
display:none!important; /* hide page reference (title) */
}

[data-tag="min-con"], [data-tag="min-con"] + .rm-query .zoom-mentions-view {
  display:none !important;  /* hide mention context (breadcrumbs) */
}

[data-tag="min-q"], 
[data-tag="min-q"] + .rm-query .rm-query-title {
  display:none !important;  /* hide the query string */
}

[data-tag="min-all"], 
[data-tag="min-all"] + .rm-query .zoom-mentions-view,
[data-tag="min-all"] + .rm-query .rm-title-arrow-wrapper,
[data-tag="min-all"] + .rm-query .rm-query-title {
  display:none !important;  /* hide everything */
}

[data-tag="minimal"] + .rm-query .rm-query-title::after,
[data-tag="min-title"] + .rm-query .rm-query-title::after,
[data-tag="min-con"] + .rm-query .rm-query-title::after{
  content: " #minimal" /* add a tag to the query string to indicate this query has been minimized */
}

/* Personal addition */
[data-tag="page-focus"], 
[data-tag="page-focus"] + .rm-query .zoom-mentions-view,
[data-tag="page-focus"] + .rm-query .rm-reference-item,
[data-tag="page-focus"] + .rm-query .rm-caret,
[data-tag="page-focus"] + .rm-query .rm-query-title {
  display:none !important;  /* hide everything */
}```
            - Content
                - Headings #Status/Enabled
                    - Preview
                        - # Heading 1
                            - ## Heading 2
                                - ### Heading 3
                    - Settings
                        - ```css
:root {
  --fnt-page-title: 		/*-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif*/;
  --fnt-h1:       			/*-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif*/;
  --fnt-h2:       			/*-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif*/;
  --fnt-h3:       			/*-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif*/;
  --fnt-size-page-title: 	22px;
  --fnt-size-h1:       		20px;
  --fnt-size-h2:       		17px;
  --fnt-size-h3:       		14px;
  --fnt-style-h1:			normal;
  --fnt-style-h2:			normal;
  --fnt-style-h3:			normal;
  --fnt-weight-h1:			500;
  --fnt-weight-h2:			500;
  --fnt-weight-h3:			500;
}```

                    - Headings
                        - ```css
h1.level2,
.rm-level2, 
.rm-heading-level-2 > .rm-block__self .rm-block__input {
  color: var(--fg-h2);
}

.rm-level1, 
.rm-heading-level-1 > .rm-block__self .rm-block__input {
  color: var(--fg-h1);
}

.rm-level3, 
.rm-heading-level-3 > .rm-block__self .rm-block__input {
  color: var(--fg-h3);
}

.roam-body .roam-app h1,
.rm-level1, 
.rm-heading-level-1 > .rm-block__self .rm-block__input {
/*  font-family: var(--fnt-h1);*/
  font-size: var(--fnt-size-h1);
  font-weight: var(--fnt-weight-h1);
  font-style: var(--fnt-style-h1);
}

h1.level2,
.rm-level2, 
.rm-heading-level-2 > .rm-block__self .rm-block__input {
/*  font-family: var(--fnt-h2)!important; */
  font-size: var(--fnt-size-h2);
  font-weight: var(--fnt-weight-h2);
  font-style: var(--fnt-style-h2);
}

.rm-level3, 
.rm-heading-level-3 > .rm-block__self .rm-block__input {
/*  font-family: var(--fnt-h3); */
  font-size: var(--fnt-size-h3);
  font-weight: var(--fnt-weight-h3);
  font-style: var(--fnt-style-h3);
}

.roam-body .roam-app h1,
.roam-body .roam-app .roam-main .roam-article .rm-title-display {
/*  font-family: var(--fnt-page-title)!important; */
  font-size: var(--fnt-size-page-title);
  color: var(--fg-h1);
}```
                - External Links #Status/Enabled
                    - ```css
.rm-alias--external {
  color: var(--fg-link);
}

.rm-alias--external:after {
  content: '↗';
}

.rm-alias--external:hover {
    text-decoration: none!important;
    border-bottom: 1px dashed;
    color: var(--cl-blue-900);
}
  
.rm-alias--external{
  color: var(--cl-blue-700);
  text-decoration: none!important;
  border-bottom: 1px solid;
}```
- From [[Roam Agile Template]]
    - #status/draft, #status/active, #status/closed
        - ```css
span.rm-page-ref[data-tag^="status/"]
{
    color: black !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    display:inline-block;
    border: 1px solid black;
    line-height: 1em;
    position:relative;
}```
    - #priority/low, #priority/medium, #priority/high
        - ```css
span.rm-page-ref[data-tag^="priority"]
{
    color: black !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    display:inline-block;
    border: 1px solid black;
    line-height: 1em;
    position:relative;
}

span.rm-page-ref[data-tag$="/low"]::before {
  content: '🔈 ';
}
span.rm-page-ref[data-tag$="/medium"]::before {
  content: '🔉 ';
}
span.rm-page-ref[data-tag$="/high"]::before {
  content: '🔊 ';
}```
    - #CAF #ADI #PMI #CnS #APC #OPV #choice #TOSCA
        - ```css
span.rm-page-ref[data-tag="CAF"],
span.rm-page-ref[data-tag="ADI"],
span.rm-page-ref[data-tag="PMI"],
span.rm-page-ref[data-tag="CnS"],
span.rm-page-ref[data-tag="APC"],
span.rm-page-ref[data-tag="OPV"],
span.rm-page-ref[data-tag="choice"],
span.rm-page-ref[data-tag="TOSCA"]
{
    color: white !important;
    padding: 3px 2px 3px 5px;
    margin-right: 12px;
    font-size: 13px;
    line-height: 1em;
    border-radius: 2px 0px 0px 2px;
    position: relative;
    background: red;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, orange, red);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, orange, red); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

span.rm-page-ref[data-tag="CAF"]::after,
span.rm-page-ref[data-tag="ADI"]::after,
span.rm-page-ref[data-tag="PMI"]::after,
span.rm-page-ref[data-tag="CnS"]::after,
span.rm-page-ref[data-tag="APC"]::after,
span.rm-page-ref[data-tag="OPV"]::after,
span.rm-page-ref[data-tag="choice"]::after,
span.rm-page-ref[data-tag="TOSCA"]::after
{
    left: 100%;
    top: 50%;
    border: solid transparent;
    content: " ";
    height: 0;
    width: 0;
    position: absolute;
    pointer-events: none;
    border-color: rgba(255,255,255,0);
    border-left-color: red;
    border-width: 11px;
    margin-top: -11px;
}

span.rm-page-ref[data-tag="CAF"]::before,
span.rm-page-ref[data-tag="ADI"]::before,
span.rm-page-ref[data-tag="PMI"]::before,
span.rm-page-ref[data-tag="CnS"]::before,
span.rm-page-ref[data-tag="APC"]::before,
span.rm-page-ref[data-tag="OPV"]::before,
span.rm-page-ref[data-tag="choice"]::before,
span.rm-page-ref[data-tag="TOSCA"]::before
{
  content: '⚙';
}
```
    - #sentiment/Neutral #sentiment/Negative #sentiment/Positive #sentiment/VeryPositive #sentiment/VeryNegative
        - ```css
span.rm-page-ref[data-tag^="sentiment/"] {
  overflow: hidden;
  white-space: nowrap;
  display: inline-block;
  margin-right: 5px;
  width: 18px;
}

span.rm-page-ref[data-tag$="/Positive"]::before {
  content: '🙂 ';
}
span.rm-page-ref[data-tag$="/VeryPositive"]::before {
  content: '😊 ';
}
span.rm-page-ref[data-tag$="/Negative"]::before {
  content: '🙁 ';
}

span.rm-page-ref[data-tag$="/VeryNegative"]::before {
  content: '😥 ';
}

span.rm-page-ref[data-tag$="/Neutral"]::before {
  content: '😐 ';
}```
    - #feedbacktype/Feature #feedbacktype/Comment #feedbacktype/Question
        - ```css
span.rm-page-ref[data-tag^="feedbacktype/"] {
  overflow: hidden;
  white-space: nowrap;
  display: inline-block;
  margin-right: 5px;
  width: 18px;
}

span.rm-page-ref[data-tag$="/Feature"]::before {
  content: '✨ ';
}
span.rm-page-ref[data-tag$="/Comment"]::before {
  content: '💬 ';
}
span.rm-page-ref[data-tag$="/Question"]::before {
  content: '❓ ';
}
```
    - Set width
        - ```css
:root {
  /* GLOBAL WIDTH FOR BLOCKS */
  --reduce-padding-right: 950px;        /* DEFAULT 568px;  Increase these two padding values to increase */
  --reduce-padding-left: 1500px;        /* DEFAULT 1032px; the global width of your blocks on the page */  
}

div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"] {
    padding-right: calc((100% - var(--reduce-padding-right)) / 2) !important;
    padding-left: calc((100% - var(--reduce-padding-left)) / 2) !important;
}

#rm-log-container {
    padding-right: calc((100% - var(--reduce-padding-right)) / 2) !important;
    padding-left: calc((100% - var(--reduce-padding-left)) / 2) !important;
}

/* fix for width when left sidebar open */
div[style*="padding-right: calc((100% - 568px) / 2); padding-left: calc((100% - 1032px) / 2);"] {
    padding-right: calc((100% - var(--reduce-padding-right)) / 2) !important;
    padding-left: calc((100% - var(--reduce-padding-left)) / 2) !important;
}

/* fix for width when left sidebar closed */
div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"] {
    padding-right: calc((100% - calc((var(--reduce-padding-right) + var(--reduce-padding-left)) / 2)) / 2) !important;
    padding-left:  calc((100% - calc((var(--reduce-padding-right) + var(--reduce-padding-left)) / 2)) / 2) !important;
}

.rm-block-text {
    max-width: 100% !important;
}

.roam-block-container {
    max-width: 100%;
}```
- Remove Query String
    - ```css
```
