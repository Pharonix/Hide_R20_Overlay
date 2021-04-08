// ==UserScript==
// @name          Roll20 Dark
// @namespace     https://openuserjs.org/scripts/Pharonix/Hide_Overlay
// @description	  Hides the Game Name Overlay Glitch.
// @author        Pharonix
// @include       https://app.roll20.net/editor*
// @include       https://app.roll20.net/campaigns/chatarchive*
// @run-at        document-start
// @version       2021.4.7.0
// @license       GPL-3.0-or-later
// ==/UserScript==
(function() {var css =`

/*
HIDE Annoying Game Name Overlay
*/

.tipsy-inner{
visibility:hidden;
}

`;
if (typeof GM_addStyle != "undefined") {
	GM_addStyle(css);
} else if (typeof PRO_addStyle != "undefined") {
	PRO_addStyle(css);
} else if (typeof addStyle != "undefined") {
	addStyle(css);
} else {

    const node = document.createElement("style");
	node.type = "text/css";
	node.innerHTML = css;

    // Note(stormy): wait for document.head to be available
    const interval = 10;
    const waitForDepts = () => {
        if(!document.head) {
            setTimeout(waitForDepts, 10);
            return;
        }

        document.head.appendChild(node);

    }
    setTimeout(waitForDepts, 10);
}
})();
(function(){
const el = document.createElement("link");
el.rel = "stylesheet";
el.href = "/css/licensed5ednd.css";
document.head.appendChild(el)
})();
