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
- 思维导图模式
    - ```css
/* Created by: @Calhistorian (Mark Robertson) */

.blockmap {
  display: flex;
  align-items: left;
  flex-direction: row;
  align-items: baseline; /* allows Azlan's path finder to not go "up" */
  justify-content: baseline;

}
 
.blockmap div {
 border:none;

} 

.blockmap .rm-block__self  {
  width: 400px; /* Adjust this value for block width */
  padding: 10px 10px;
}

.blockmap .rm-block__children {
  margin-top: 5px;
  margin-bottom: 5px;
}

/* Horizontal Scrolling */
.roam-body-main > div  {
  overflow-x: scroll !important;
}```
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
- 
