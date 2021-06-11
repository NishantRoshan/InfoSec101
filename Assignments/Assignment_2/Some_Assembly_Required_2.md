# PicoGym Web Exploitation Writeup

Author: [Nishant Roshan](https://github.com/NishantRoshan)

Challenge Page: [Some Assembly Required 2](http://mercury.picoctf.net:53929/index.html)

## Walkthrough
1) Firstly viewed the source code. It had the html code and the link to js code of the program. There was nothing special in the html code, was just a few lines written in html.
2) Then opened the js code. It has js code all jumbled up. Used the online js deobfuscator (https://www.dcode.fr/javascript-unobfuscator) to obtain the js code. Then used the online js beautifier(https://html-cleaner.com/js/). But still even though did not get anything important. ☹️☹️
The final js decrypted code found was
use strict';
var _0x6d8f = ["copy_char", "value", "207aLjBod", "1301420SaUSqf", "233ZRpipt", "2224QffgXU", "check_flag", "408533hsoVYx", "instance", "278338GVFUrH", "Correct!", "549933ZVjkwI", "innerHTML", "charCodeAt", "./aD8SvhyVkb", "result", "977AzKzwq", "Incorrect!", "exports", "length", "getElementById", "1jIrMBu", "input", "615361geljRK"];
var _0x5c00 = function _getCompositionValue(key, value) {
key = key - 195;
var value = _0x6d8f[key];
return value;
};
(function(data, oldPassword) {
var toMonths = _0x5c00;
for (; !![];) {
try {
var userPsd = -parseInt(toMonths(200)) * -parseInt(toMonths(201)) + -parseInt(toMonths(205)) + parseInt(toMonths(207)) + parseInt(toMonths(195)) + -parseInt(toMonths(198)) * parseInt(toMonths(212)) + parseInt(toMonths(203)) + -parseInt(toMonths(217)) * parseInt(toMonths(199));
if (userPsd === oldPassword) {
break;
} else {
data["push"](data["shift"]());
}
} catch (_0x4f8a) {
data["push"](data["shift"]());
}
}
})(_0x6d8f, 310022);
var _exports = void 0;
(async function() {
var getDestroyAccountUrl = _0x5c00;
var _0x1adb5f = await fetch(getDestroyAccountUrl(210));
var tiledImageBRs = await WebAssembly["instantiate"](await _0x1adb5f["arrayBuffer"]());
var tiledImageBR = tiledImageBRs[getDestroyAccountUrl(204)];
_exports = tiledImageBR[getDestroyAccountUrl(214)];
})();
function onButtonPress() {
var navigatePop = _0x5c00;
var PL$42 = document[navigatePop(216)](navigatePop(218))[navigatePop(197)];
var PL$41 = 0;
for (; PL$41 < PL$42["length"]; PL$41++) {
_exports[navigatePop(196)](PL$42[navigatePop(209)](PL$41), PL$41);
}
_exports["copy_char"](0, PL$42[navigatePop(215)]);
if (_exports[navigatePop(202)]() == 1) {
document["getElementById"](navigatePop(211))[navigatePop(208)] = navigatePop(206);
} else {
document[navigatePop(216)](navigatePop(211))["innerHTML"] = navigatePop(213);
}
}
;
3) Then followed the usual algorithm of inspection of the webpage (do this via right click)
4) Went one after the other to sources part. There were two files (one html code and one the js code) in the 1st folder. In the 2nd folder named **wasm**, was some code written. Taking clue from Some Assembly Required 1, the last line of this folder might have the flag🧐🧐.  
5) But here there was not the direct flag. Instead it was encrypted in some cipher, which I didn't get what kind of cypher it is. [This](file:///C:/Users/AYUSHI%20SNEHA/Desktop/Nishant/example.html) link has the ss of the page on inspection.
6) Always for any kind of cipher to be decrypted, use cyber chef (best online cipher decrypt) Link in resources part. It can decrypt, even without us telling the type of cipher.
7) Decrypt the cipher to get the flag.  😇  😇 
 
## Flag    
picoCTF{6f3bd18312ebf1e48f12282200948876}

## Useful resources
1) [js deobfuscator](https://www.dcode.fr/javascript-unobfuscator)
2) [js beautifier](https://html-cleaner.com/js/)
3) [cyber chef](https://gchq.github.io/CyberChef/)

## suggested modification
We dont't need to think much to make this level more difficult. It is already present as vol3 and vol4 of Some Assembly Required. Just go and solve them **😜** 
