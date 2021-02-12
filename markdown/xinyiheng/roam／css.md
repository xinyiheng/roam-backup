- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam hendrerit elit in erat congue, quis efficitur massa ultrices. Aliquam volutpat lobortis dapibus. Cras lacus ligula, maximus luctus porta rutrum, viverra rhoncus elit. Fusce sit amet nulla tincidunt sapien vulputate mattis in ac felis. Vestibulum dictum eu velit id pulvinar. Integer lacus nulla, ornare vitae mauris id, vulputate aliquam diam. Aliquam ullamcorper tempor arcu a malesuada. Nulla facilisi. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in condimentum sapien, ac feugiat mi. Nulla facilisi. Integer ut velit metus. Donec lacinia mattis imperdiet. Pellentesque vulputate augue sit amet egestas hendrerit. Duis ultricies auctor libero id ornare. #bq
- Code
    - Definition of the blockquote:#[[bq]]
        - css
 /*设置带有某种标签的block格式*/
[data-page-links*="bq"] {
  background-color: rgb(244,242,242);
  border-left: 5px solid rgb(255,204,111);
  padding-left: 10px;
  
}
    - Hiding the tag
        - css

[data-tag="bq"] {
display:none;
  }
- Using Roam/CSS to display a list as grid or in rows
via[Using Roam/CSS to display a list as grid or in rows](https://www.loom.com/share/06b03473bcda4728b5bef40929e5012f)
[[20201230]] 上午10:14官方推出的一些css样式，用视频的形式展示出来的，比较直观
- ## Element Class Detail 发现没有关联的概念
    - Class: `exact-word-match`
        - Criteria
            - Case-Sensitive Match
            - Match is a complete word, not part of a word
            - Word is not already linked in a parent block
        - Example
            - You have a page called `link` and it matches a word `link`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2Fim9emHjoe1.png?alt=media&token=278bd9e0-57fe-4bec-896e-17cb9cfefb4a)
        - Default Style
            - These are underlined in the same color as the text.
                - In the example, the color is black.
    - Class: `fuzzy-word-match`
        - Criteria
            - Case-insensitive match
        - Example
            - You have a page called `link` and it matches a word `LINK`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2F0Wf5trJvpB.png?alt=media&token=4eec4fdb-2f0b-45f1-b159-d6f886320376)
        - Default Style
            - These are underlined in css gray
    - Class: `partial-word-match`
        - Criteria
            - Match found but it is a substring of another word
        - Example
            - You have a page called `link` that matches in a word `linked`
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2FNsFoGrgFKM.png?alt=media&token=270efc93-0749-47c4-aa53-4b7b4beabaff)
        - Default Style
            - These are underlined in css lightgray
    - Class: `redundant-word-match`
        - Criteria
            - Any match where the matched page is linked in a parent block. Creating this link again would be redundant.
        - Example
            - You have a page called `link` and the match is nested under a block already referencing that page.
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Ftylerwince%2FxNGU82eQvP.png?alt=media&token=28ab0832-404b-4b2f-b3ab-0a0bc9eaaf4b)
        - Default Style
            - These have a transparent underline, essentially no indicator. If you want them to show, you can change the `text-decoration-color` to whatever you prefer in roam/css
    - match
        - ```css
.exact-word-match.unlink-finder,
.unlink-finder-legend.exact-word-match.unlink-finder {
  background-color: lightblue;
  border-radius: 2px;
  text-decoration: none !important;
}
.fuzzy-word-match.unlink-finder,
.unlink-finder-legend.fuzzy-word-match.unlink-finder {
  background-color:  pink!important;
  text-decoration: none !important;
}
.partial-word-match.unlink-finder,
.unlink-finder-legend.partial-word-match.unlink-finder {
  background-color:  lightgreen !important;
  text-decoration: none !important;
}
.redundant-word-match.unlink-finder,
.unlink-finder-legend.redundant-word-match.unlink-finder {
  background-color: lightyellow !important;
  text-decoration: none !important;
}```
        - 
        - .unlink-finder-legend.exact-word-match.unlink-finder {
            - background-color: darkgreen;
            - border-radius: 2px;
            - text-decoration: none !important;
        - }
        - .fuzzy-word-match.unlink-finder,
        - .unlink-finder-legend.fuzzy-word-match.unlink-finder {
            - background-color:  darkorange !important;
            - text-decoration: none !important;
        - }
        - .partial-word-match.unlink-finder,
        - .unlink-finder-legend.partial-word-match.unlink-finder {
            - background-color:  brown !important;
            - text-decoration: none !important;
        - }
- 美化youtube时间戳的按钮分享一个Andy Mode的CSS和几个js插件https://github.com/GitMurf/masonry-vanilla#masonry-vanilla
    - ```css
.timestamp-control{
  background-color: rgba(108,109,36,0.1); 
  color: rgb(251,106,13);
  margin-right: 8px;
  margin-top: 0px;
  margin-left: 0px;
  margin-bottom: 5px;

  border-radius: 50% !important;
  border-style: inset;  
  border-color: #FF3200;
  font-size: 0.9em;
}
.timestamp-control:hover {
  background-color: rgba(108,109,36,0.25); 
  border-style: outset;  
  color: #FFFFFF;
}```
- 新的css    --right-sidebar-drag-bg: #337ac6;分享一个Andy Mode的CSS和几个js插件https://github.com/GitMurf/masonry-vanilla#masonry-vanilla

    - ```css

:root {
    --main-left-bg: #CCCFD1;
    --main-left-border: 3px solid rgb(30,4,4);
    --right-sidebar-bg: #773535(247 248 249);
    --masonry-bg: #FBFBF7;
    --masonry-scrollbar-bg: lightgrey;
    --masonry-resizer-color: lightgrey;
    --masonry-startWidth: 400px;
    /* DEFAULT: 550px; Change this to "unset" if you DON'T want the sidebar pages to be reset in grid like format each time */
    --masonry-minWidth: 440px;
    --masonry-maxWidth: 1200px;
    --masonry-startHeight: 234px;
    /* DEFAULT: 243px; Change this to "unset" if you DON'T want the sidebar pages to be reset in grid like format each time */
    --masonry-minHeight: 200px;
    --masonry-border: 2px double #ED5A2A;
    --closed-bullet-color: 4px solid #CED9E0;
    --code-color: crimson;
}
div.roam-app>div.roam-sidebar-container {
    display:none;
}
div.roam-app>div.flex-h-box>div.roam-main>div.roam-body-main {
    background-color: #E9FAEA;
}
#right-sidebar, div.roam-app>div.flex-h-box {
    background-color: var(--right-sidebar-bg);
}

#roam-right-sidebar-content {
    overflow: auto !important;
}
.sidebar-content {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 99%;
    align-content: flex-start;
}

.sidebar-content>div:not(.rm-dnd-separator) {
    margin-bottom: 10px !important;
    display: flex;
    background-color: var(--masonry-bg);
    max-height: 100%;
    margin-left: 15px;
    align-self: flex-start;
    /* So pages can be diff widths in a single column */
    border-radius: 12px;
    border: var(--masonry-border);
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator) {
    border-bottom: unset !important;
    height: 100%;
    padding-top: 10px;
    padding-bottom: 10px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:first-child {
    height: 40px;
    min-width: calc(var(--masonry-minWidth) + 40px);
    align-items: center !important;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2) {
    height: calc(100% - 40px);
}

/*NOTE: .rm-sidebar-outline and .rm-reference-main are at same level and so need to be addressed with div > div... as opposed to direct .classnames */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2) {
    resize: both;
    overflow-y: auto;
    width: var(--masonry-startWidth);
    min-width: var(--masonry-minWidth);
    max-width: var(--masonry-maxWidth);
    height: var(--masonry-startHeight);
    min-height: var(--masonry-minHeight);
    max-height: 100%;
    margin-right: 8px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)>div:nth-child(2) {
    padding-bottom: 40px;
    margin-left: -8px !important;
}

.sidebar-content .rm-reference-main>div {
    margin-left: 0px !important;
    margin-right: 5px !important;
    padding-bottom: 40px;
}

/* SCROLLBAR */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar {
    width: unset;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar:hover {
    background-color: var(--masonry-bg);
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-resizer {
    border-style: solid;
    border-color: transparent var(--masonry-resizer-color) var(--masonry-resizer-color) transparent;
    background-color: var(--masonry-bg);
    border-width: 3px;
}

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar-button, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar-thumb, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar-track, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar-track-piece, .sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2)::-webkit-scrollbar-corner {
    display: none;
}

/*Make the scrollbar smaller but keep the resize button the same*/

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div:nth-child(2)>div:nth-child(2):hover::-webkit-scrollbar-thumb {
    display: block;
    border-radius: 12px;
    background-color: var(--masonry-scrollbar-bg);
    border-style: solid;
    border-width: 6px;
    border-color: var(--masonry-bg);
}

/* Focus/zoom breadcrumb trail */

.roam-body-main .roam-article .zoom-path-view {
    margin-top: 10px;
}

/* Don't let images extend outside box */

.rm-inline-img__resize, .react-resizable {
    max-width: 100%;
}

/* When long page titles or block refs are in sidebar they need to be shrunk */

.sidebar-content>div:not(.rm-dnd-separator)>div:not(.rm-dnd-separator)>div.flex-h-box.window-headers>div:nth-child(2) {
    max-width: calc(var(--masonry-minWidth) - 10px);
    max-height: 3em !important;
    overflow: hidden;
}

/* Drag n Drop */

.sidebar-content>div.rm-dnd-separator {
    left: 16px;
    top: -3px;
    width: calc(var(--masonry-minWidth));
}

.sidebar-content>div>div.rm-dnd-separator {
    right: 100%;
    top: 100%;
}

.sidebar-content .rm-dnd-separator .rm-dnd-drop-bar {
    top: 3px;
    left: 1px;
    background-color: var(--right-sidebar-drag-bg);
}

.sidebar-content .rm-dnd-separator {
    width: unset;
}

.rm-dnd-drop-area, .rm-dnd-drop-bar {
    min-width: calc(var(--masonry-minWidth) + 55px);
}

/* The new indent lines were showing on top of search bar */

/* Abhay said that him and jeff harris set to 8, but I needed to set to 4 to work */

.rm-multibar {
    z-index: 4;
}
Search...
```
- 新的css附加1
    - ```css

/* Extend the main page wider to allow for blocks to be wider  */

div[style*="padding-right: calc((100% - 800px) / 2); padding-left: calc((100% - 800px) / 2);"], div[style*="padding-right: calc((100% - 568px) / 2); padding-left: calc((100% - 1032px) / 2);"] {
    /* FULL WIDTH
    padding-right: calc((100% - 3400px) / 2) !important;
    padding-left: calc((100% - 3400px) / 2) !important;
  */
    padding-right: calc((100% - 1500px) / 2) !important;
    padding-left: calc((100% - 1500px) / 2) !important;
}

/* Block text widths to extend block text wider for when you make the page wider with the CSS above  */

.roam-block-container {
    max-width: unset;
}

#right-sidebar .rm-block-children.rm-block__children.rm-level-0>div.roam-block-container, #right-sidebar div.zoom-path-view+div>div.roam-block-container {
    width: 98%;
}

.rm-block-text {
    max-width: unset;
}

#right-sidebar div.rm-zoom.zoom-path-view {
    width: 98%;
}

/* Allow images to resive full width */

.hoverparent[style^="width: 580px;"], .hoverparent[style^="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

.rm-inline-img, .react-resizable[style^='width: 580px;'], .react-resizable[style^='width: 720px;'] {
    width: 100% !important;
}

/* Override image, iframe, pdf resize form abhay 1-30-21 */

div[style*="width: 580px;"], div[style*="width: 720px;"] {
    width: 100% !important;
    max-width: 1100px !important;
}

div[style*="height: 720px;"] {
    height: 85vh !important;
}

/* MOVING MENU AND SEARCH BOX TO THE UPPER RIGHT WHEN SIDEBAR IS OPEN (instead of default middle of page) */

.roam-body-main {
    margin-top: 4px;
}

.rm-topbar {
    border-bottom: 0;
    padding-right: 20px;
    width: 100vw;
    z-index: 5;
    position: fixed;
    right: 0;
}

#roam-right-sidebar-content {
    margin-top: 20px;
}

/* Search bar wide when typing in it */

/* These account for left sidebar being open and making sure search bar stays on top of it */
.roam-sidebar-container.noselect:hover {
    z-index: 1001;
}
.rm-topbar {
    z-index: 1000;
}

.rm-find-or-create-wrapper:focus-within {
    flex: 0 1 77% !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li>span {
    max-height: 42px !important;
    word-break: break-word !important;
    overflow: hidden !important;
    display: inline-block !important;
}

.bp3-overlay-open ul.bp3-menu .rm-menu-item li {
    list-style-type: none !important;
    margin-left: -35px;
}

/* Buttons / Icons in menu area by search bar */

/* Filter button was kind of high and to the left */

.rm-topbar .bp3-button .bp3-icon.bp3-icon-filter {
    margin-top: 4px;
    margin-right: -18px;
}

/* Fixing the sidebar close button to show on very right of menu bar */

#right-sidebar .bp3-icon-menu-open {
    z-index: 1001;
    padding-top: 4px !important;
}
.rm-topbar {
    padding-right: 30px;
}

/* Add dashed line on hover of sidebar resizer line in middle of page */

.rm-resize-handle:hover {
    opacity: 0.4 !important;
    border-right: 2px dashed #1b1a23 !important;
    padding-left: 5px;
}

/* The "all collapse/expand" invisible line to very left of blocks */

.rm-level-0>.rm-multibar {
    opacity: 0.25;
}

/* Hide "Outline of: " in the sidebar except for block references because otherwise nowhere to grab for drag n drop. */

div.sidebar-content div.flex-h-box.window-headers>div:nth-child(2)>span:first-child:not([style^="margin-right: 6px"]) {
    display: none;
}
Search...
```
- 新的css附加2
    - ```css

/* Hide graph button in top bar menu area */

.bp3-button.bp3-minimal.bp3-icon-menu.pointer.bp3-small.rm-open-left-sidebar-btn {
  	display: none;
}


/* ***** SEARCH BAR RESULTS FORMATTING ***** */

/* page results from search bar */

.rm-search-title {
    color: rgb(40,13,204) !important;
}

/* Search results text */

li.rm-search-list-item>span {
    color: initial !important;
}

/* Search results found text highlight */

span[style*="background-color: yellow"] {
    background-color: lemonchiffon !important;
    color: initial !important;
    padding-left: 2px !important;
    padding-right: 2px !important;
    margin-left: 2px !important;
    margin-right: 2px !important;
    /*font-weight: bold !important;*/
}

/* search box for block ref and page links move to left (beginning of block) */

.bp3-elevation-3 {
    max-height: 500px !important;
    width: 100% !important;
    max-width: 100% !important;
    left: -6px !important;
    /* This moves the search box back to left in line with the bullets so doesn't overflow when towards right edge of screen */
}

.rm-autocomplete-result {
    word-break: unset;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

/* block ref stuff */

/* Undo the default Roam css on block refs */

.rm-block-ref {
    padding: unset;
    margin: unset;
    display: unset;
    border-bottom: blue;
    cursor: alias;
}

/* Limited this down to block refs excluding tables (weird attribute table issue where it adds attribute children blocks as block refs) */

.rm-block-ref.dont-focus-block {
    color: var(--block-reference-text) !important;
    border-bottom: none !important;
    border-right-color: #0079FF !important;
    border-right-width: 1px !important;
    border-right-style: dashed !important;
    padding-right: 5px !important;
    border-left-color: #0079FF !important;
    border-left-width: 1px !important;
    border-left-style: dashed !important;
    padding-left: 5px !important;
}

.rm-block-ref.dont-focus-block:hover {
    background-color: var(--block-ref-hover-bg) !important;
    border-bottom: unset !important;
}

/* get rid of the weird SPAN background color in attribute table cells */

div.roam-table span[style*="position: absolute; opacity: 0.1; background-color: rgb(14, 90, 138); inset: 0px;"] {
    background-color: unset !important;
}

/* The bullet background color on closed bullets with children */

.rm-bullet.rm-bullet--closed .rm-bullet__inner {
    border: var(--closed-bullet-color);
}

/* Updates to highlighted text in Roam with ^^text^^ */

.rm-highlight {
    margin: unset;
    padding: 2px 4px;
}

del, strike, s {
    color: grey;
}

/* Inline Code */

code {
    color: var(--code-color);
}

/* All of Murf's added icons / buttons */

.murf-icon {
    margin-top: unset; /* 2px; */
    margin-left: unset; /* 8px; */
    margin-right: unset; /* -6px; */
}

/* Rainbow Indentation by Abhay from Dracula (tweaked by Murf) */

/* https://abhayprasanna.github.io/rainbow-indent.css */

/* https://abhayprasanna.github.io/rainbow-indent-core.css */

:root {
    /* My colors */
    --box-shadow-values:5px 0px 20px -30px;
    /* Set to "none" to remove shadow... or 25px 0px 20px -30px; */
    --indent1: #07BC1C;
    --indent2: #FF0900;
    --indent3: #5BC9D7;
    --indent4: violet;
    --indent5: orange;
    --indent6: #01A80E;
    --indent7: #0079FF;
    --indent8: pink;
    --indent9: black;
    --indent10: springgreen;
    --indent11: #FF0900;
    --indent12: #5BC9D7;
    --indent13: violet;
    --indent14: orange;
    --indent15: #01A80E;
    --indent16: #0079FF;
    --indent17: pink;
    --indent18: black;
    /* Abhay colors
    --indent1: #5F388BAD;
    --indent2: #4A57BAAD;
    --indent3: #48864DAD;
    --indent4: #A7A15AAD;
    --indent5: #AD7E48AD;
    --indent6: #A5494FAD;
    --indent7: #634071AD;
    --indent8: #303472AD;
    --indent9: #395C45AD;
    --indent10: #7C7948AD;
    --indent11: #7D5039AD;
    --indent12: #A5494FAD;
    --indent13: #706597AD;
    --indent14: #657D91AD;
    --indent15: #6D8D76AD;
    --indent16: #A09A84AD;
    --indent17: #987174AD;
    --indent18: #8B5F78AD;
  */
}

/* Level 1 */

.rm-level-1>div, .rm-level-19>div, .rm-level-37>div, .rm-inline-references>.rm-multibar {
    border-right-color: var(--indent1);
    box-shadow: var(--box-shadow-values) var(--indent1) inset;
}

/* Level 2 */

.rm-level-2>div, .rm-level-20>div, .rm-level-38>div {
    border-right-color: var(--indent2);
    box-shadow: var(--box-shadow-values) var(--indent2) inset;
}

/* Level 3 */

.rm-level-3>div, .rm-level-21>div, .rm-level-39>div {
    border-right-color: var(--indent3);
    box-shadow: var(--box-shadow-values) var(--indent3) inset;
}

/* Level 4 */

.rm-level-4>div, .rm-level-22>div, .rm-level-40>div {
    border-right-color: var(--indent4);
    box-shadow: var(--box-shadow-values) var(--indent4) inset;
}

/* Level 5 */

.rm-level-5>div, .rm-level-23>div, .rm-level-41>div {
    border-right-color: var(--indent5);
    box-shadow: var(--box-shadow-values) var(--indent5) inset;
}

/* Level 6 */

.rm-level-6>div, .rm-level-24>div, .rm-level-42>div {
    border-right-color: var(--indent6);
    box-shadow: var(--box-shadow-values) var(--indent6) inset;
}

/* Level 7 */

.rm-level-7>div, .rm-level-25>div, .rm-level-43>div {
    border-right-color: var(--indent7);
    box-shadow: var(--box-shadow-values) var(--indent7) inset;
}

/* Level 8 */

.rm-level-8>div, .rm-level-26>div, .rm-level-44>div {
    border-right-color: var(--indent8);
    box-shadow: var(--box-shadow-values) var(--indent8) inset;
}

/* Level 9 */

.rm-level-9>div, .rm-level-27>div, .rm-level-45>div {
    border-right-color: var(--indent9);
    box-shadow: var(--box-shadow-values) var(--indent9) inset;
}

/* Level 10 */

.rm-level-10>div, .rm-level-28>div, .rm-level-46>div {
    border-right-color: var(--indent10);
    box-shadow: var(--box-shadow-values) var(--indent10) inset;
}

/* Level 11 */

.rm-level-11>div, .rm-level-29>div, .rm-level-47>div {
    border-right-color: var(--indent11);
    box-shadow: var(--box-shadow-values) var(--indent11) inset;
}

/* Level 12 */

.rm-level-12>div, .rm-level-30>div, .rm-level-48>div {
    border-right-color: var(--indent12);
    box-shadow: var(--box-shadow-values) var(--indent12) inset;
}

/* Level 13 */

.rm-level-13>div, .rm-level-31>div, .rm-level-49>div {
    border-right-color: var(--indent13);
    box-shadow: var(--box-shadow-values) var(--indent13) inset;
}

/* Level 14 */

.rm-level-14>div, .rm-level-32>div, .rm-level-50>div {
    border-right-color: var(--indent14);
    box-shadow: var(--box-shadow-values) var(--indent14) inset;
}

/* Level 15 */

.rm-level-15>div, .rm-level-33>div, .rm-level-51>div {
    border-right-color: var(--indent15);
    box-shadow: var(--box-shadow-values) var(--indent15) inset;
}

/* Level 16 */

.rm-level-16>div, .rm-level-34>div, .rm-level-52>div {
    border-right-color: var(--indent16);
    box-shadow: var(--box-shadow-values) var(--indent16) inset;
}

/* Level 17 */

.rm-level-17>div, .rm-level-35>div, .rm-level-53>div {
    border-right-color: var(--indent17);
    box-shadow: var(--box-shadow-values) var(--indent17) inset;
}

/* Level 18 */

.rm-level-18>div, .rm-level-36>div, .rm-level-54>div {
    border-right-color: var(--indent18);
    box-shadow: var(--box-shadow-values) var(--indent18) inset;
}
Search...
```
- kanban
    - ```css

.kanban-board {
  background-color: #FFDB3A;
  max-height: 600px; 
  overflow-x: auto;
  overflow-y: auto;
}

.kanban-column {
  background-color: rgba(248,227,187,0.98);
}

.kanban-card {
  box-shadow: 0 1px 4px 0 rgba(21, 27, 38, 0.08);
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(21, 27, 38, 0.08);
}

roam-block-container rm-block rm-block--mine rm-block--open rm-not-focused block-bullet-viewroam-block-container rm-block rm-block--mine rm-block--open rm-not-focused block-bullet-view.kanban-card:hover {
  box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
  transform: translateY(-1px);
}

.kanban-title {
  text-align: left;
  margin: 0px 8px;
  font-weight: 700px;
  border-bottom: none;
}```
