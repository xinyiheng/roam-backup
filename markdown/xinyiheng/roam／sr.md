- ### suggestions
    - __(Feel free to delete anything in this section.)__
    - links
        - [PLUGIN PAGE](https://roamresearch.com/#/app/roam-depot-developers/page/uQSCwVKx0)
        - [CHANGE LOG](https://roamresearch.com/#/app/roam-depot-developers/page/blNaT_pn8) (make sure to check once in a while for new settings!)
        - [CARD BANK](https://roamresearch.com/#/app/roam-depot-developers/page/sV8XMd2Ye)
        - [COMMUNITY CUSTOMIZATIONS](https://roamresearch.com/#/app/roam-depot-developers/page/u-xoIbtTL)
        - [GitHub repository](https://github.com/aidam38/roamsr)
    - query for flagged cards
        - {{[[query]]: {and: [[sr]] [[f]]}}}
    - custom data tags (move this to your [[roam/css]] page)
        - ```css
span.rm-page-ref[data-tag="sr"] {
    background: #0059B1;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}```
- ### settings
    - {{[[roam/js]]}}
        - ```javascript
window.roamsrUserSettings = {};

/* ====== MAIN SETTINGS ====== */

// Main tag used to add cards.
// Type: String
roamsrUserSettings.mainTag = "sr";

// Tag used to flag cards. 
// Cardblocks with this tag won't get shown in review (meant for rewrite)
// Type: String
roamsrUserSettings.flagTag = "f";

// Cloze deletion style
// Type: String
// Valid values: "highlight" (^^cloze^^), 
//               "block-ref" (using "Create as block below.")
roamsrUserSettings.clozeStyle = "highlight";

/* ====== DEFAULT DECK ====== */
roamsrUserSettings.defaultDeck = {};

// Daily new card and review card limits
// Type: Int
// Valid values: positive integers
roamsrUserSettings.defaultDeck.newCardLimit = 20;
roamsrUserSettings.defaultDeck.reviewLimit = 50;

// Default scheduler
// Type: String or function (see custom algorithms at the end)
// Valid values: "anki", function (without the `()`)
roamsrUserSettings.defaultDeck.scheduler = "anki"

// Default scheduler config
// For more info on Anki, see: 
// https://faqs.ankiweb.net/what-spaced-repetition-algorithm.html
roamsrUserSettings.defaultDeck.config = {
  defaultFactor: 2.5,
  firstFewIntervals: [1, 6],
  factorModifier: 0.15,
  easeBonus: 1.3,
  hardFactor: 1.2,
  minFactor: 1.3,
  jitterPercentage: 0.05,
  maxInterval: 50 * 365,
  responseTexts: ["Again.", "Hard.", "Good.", "Easy."]
};

/* ====== CUSTOM DECKS ====== */
// The actual array of custom decks is at the end!

/* Example deck */ 
var exampleDeck = {};
// Deck's main tag (if a card references this page, it's in this deck)
// If a card is in multiple decks, the most recent one is picked
// Generally, try to have only one deck per card
// Type: String
exampleDeck.tag = "mydeck";

// Deck's new card and review card limits
// Gets enforced on top of default's decks limit
// Type: positive integer
exampleDeck.newCardLimit = 10;
exampleDeck.reviewLimit = 30;

// Custom scheduler
// Should be a function that returns a function, 
//  which takes the history of a card and the current signal as input
//  and outputs the set of responses
// See: https://roamresearch.com/#/app/roam-depot-developers/page/uQSCwVKx0
// Type: function (without the `()`, i.e. not the return value, but the function itself)
exampleDeck.scheduler = (config) => {
  // Configure your scheduler using config...
  
  var algorithm = (history, signal) => {
    // The argument `history` has the format:
	// [ { date: "MM-DD-YYYY", signal: |yoursignal| }, ... ] (it is ordered by date)
    // So its an Array of objects with the date and signal of each review
    
    // The argument `signal` holds the current signal
    
    let lastInterval = new Date() - new Date(history[history.length - 1].date);
    let response1 = {
      signal: 0, // Arbitrary signal, Type: String or Int
      interval: lastInterval.getDate(), // Next interval, Type: Int
      responseText: "Same as last time.", // Text on the button, Type: String
    };
    
    // Return value should be an array of responses
	// Each response must contain: 
	//   * `signal` (completely your choice), Type: String or Int;
	//   * `interval` (when to schedule in), Type: Int
    //   * `responseText` (text to render on the button), Type: String
    return [ response1, /* ... other responses */ ]
  }
  return algorithm;  
};

// Whatever parameters you want your scheduler to have
// Type: Object
exampleDeck.config = {};

// Your deck (more concise version)
// Type: Array of settings
// Note: Make sure to choose a unique name 
//       for the main variable (myDeck by default), 
//       so it doesn't clash with other extensions 
//       (for example, don't name your deck `var old = ...`)
var myDeck = {
  tag: "",
  scheduler: "anki",
  config: {},
  newCardLimit: 0,
  reviewLimit: 0
}

console.log("🗃️ Loaded roam/sr settings.")```
- ### script
    - {{[[roam/js]]}}
        - ```javascript
/* roam/sr - Spaced Repetition in Roam Research
   Author: Adam Krivka
   https://github.com/aidam38/roamsr
*/

var roamsrID = "roamsr-script";
var oldRoamSR = document.getElementById(roamsrID);
if (oldRoamSR) oldRoamSR.remove();
var s = document.createElement('script');
	s.type = "text/javascript";
	s.id = roamsrID;
    s.src =  "https://serene-williams-db0c75.netlify.app/js/stable.js";
  	s.async = true;
document.getElementsByTagName('head')[0].appendChild(s);```
- ### [[roam/css]]
    - ```css
/* Uncomment to enable style. */

 GLOBAL STYLING *
.roam-app, .roam-topbar {
  background-color: #eeeeee !important;
} *

/* HIDING BREADCRUMS */
/* .roam-article .rm-zoom {
  display: none;
} */

/* HIDING TOPBAR */
/* .rm-topbar {
  display: none;
} */

/* HIDING THE #sr TAG */
/* span.rm-page-ref[data-tag="sr"] {
  display: ;
} */

/* DISABLING ROAM TOOLKIT */
/* .roam-toolkit--hint0::after,
.roam-toolkit--hint1::after,
.roam-toolkit--hint2::after,
.roam-toolkit--hint3::after,
.roam-toolkit--hint4::after,
.roam-toolkit--hint5::after,
.roam-toolkit--hint6::after,
.roam-toolkit--hint7::after,
.roam-toolkit--hint8::after,
.roam-toolkit--hint9::after,
.roam-toolkit--hint10::after {
  content: "";
}

.roam-toolkit-block-mode--highlight {
  background-color: inherit;
} */```
