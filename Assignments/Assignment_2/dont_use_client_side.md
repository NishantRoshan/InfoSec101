# PicoGym Web Exploitation Writeup

Author: [Nishant Roshan](https://github.com/NishantRoshan)

Challenge Page: [dont-use-client-side](http://jupiter.challenges.picoctf.org:29835)
## Walkthrough
There is a link given in the question and it is mentioned to entre into the super secure portal. Opening the the site we entre a page where a password is asked for. The first step to any web expolitation challenge is to view the source code of the webpage. Do ctrl+u to view the source code. This part of the js code attracted my attention :
 if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == '723c') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_7') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == 'e}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
 Clearly this was some kind of flag, but in jumbled order. Rearrange the flag as per the numbers mentioned in the split. More about split method in js can be found here https://www.w3schools.com/jsref/jsref_split.asp 
 Finally rearranging the split, we get the flag. 😇😇😇

## Flag
picoCTF{no_clients_plz_7723ce}

## Useful resources 
1) How to inspect source code of a webpage in any browser : https://neilpatel.com/blog/how-to-read-source-code/
2) How to understand the split command in js : https://www.w3schools.com/jsref/jsref_split.asp

## Suggested modifications 
Even without knowing much about splitting method, the level could be solved. It could have been more difficult if the js part were encrypted and/or the flag was also written encrypted. In that case it would not be directly visible that flag is on the source code itself, unless someone decrypts the js. More about encrypting js code : https://stackoverflow.com/questions/1020368/how-can-i-hide-or-encrypt-javascript-code
