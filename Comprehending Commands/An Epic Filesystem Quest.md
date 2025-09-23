# Comprehending Commands

## An Epic Filesystem Quest
We are given a scavenger hunt which we have to solve using hints given by the system using cd, ls and cat. The first clue is to use / as our working directory and find a file named clue or something similar using ls, we are then supposed to use the clues till we get the flag. 

### Solve
**Flag:** `pwn.college{845yaut8BfJlaiu7Fqcrjizwljd.QX5IDO0wSN2gjNzEzW}`

I initally followed the hints that was to use / as working directory and then execute ls to see the file named LEAD. On reading LEAD using cat, I got a path for the next clue and it said that we can't cd into the directory. Hence, i used la to check the contents of the directory and then used cat to read it to obtain the next clue. The clue gave another path for the next clue which was again trapped hence i used the same process. The next clue gave another path and said that the next clue was delayed i.e, we have to use cd. So, i cd'ed into the directory and read the file which was close to being a clue, this gave the next clue. This clue said that the next clue was hidden and hence I cd'ed into the directory and then executed ls -a to see all files starting with a '.'. I, then, used cat to read the next clue. I had to use these 3 processes over again a few more times before I found the final clue and eventually the flag. 

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
LEAD  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat LEAD
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/tools/testing/selftests/ftrace/test.d/event

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/tools/testing/selftests/ftrace/test.d/event
TRACE-TRAPPED  event-enable.tc  event-pid.tc  subsystem-enable.tc  toplevel-enable.tc  trace_printk.tc
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/tools/testing/selftests/ftrace/test.d/event/TRACE-TRAPPED
/opt/linux/linux-5.4/tools/testing/selftests/ftrace/test.d/event/TRACE-TRAPPED
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/tools/testing/selftests/ftrace/test.d/event/TRACE-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/include/generated/uapi/linux

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/include/generated/uapi/linux
SNIPPET-TRAPPED  version.h
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/include/generated/uapi/linux/SNIPPET-TRAPPED 
/opt/linux/linux-5.4/include/generated/uapi/linux/SNIPPET-TRAPPED
hacker@commands~an-epic-filesystem-quest:/$ /opt/linux/linux-5.4/include/generated/uapi/linux/SNIPPET-TRAPPED 
bash: /opt/linux/linux-5.4/include/generated/uapi/linux/SNIPPET-TRAPPED: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/generated/uapi/linux/SNIPPET-TRAPPED 
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Size3

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Size3
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Size3$ ls
ALERT  Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Size3$ cat ALERT
Congratulations, you found the clue!
The next clue is in: /usr/share/mysql/russian

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Size3$ cd /usr/share/mysql/russian
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/russian$ ls -a
.  ..  .WHISPER  errmsg.sys
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/russian$ cat .WHISPER 
Great sleuthing!
The next clue is in: /usr/share/vim/vim81/keymap

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/russian$ ls /usr/share/vim/vim81/keymap
NUGGET-TRAPPED              czech_utf-8.vim         hebrewp_utf-8.vim            russian-dvorak.vim          slovak.vim
README.txt                  dvorak.vim              kana.vim                     russian-jcuken.vim          slovak_cp1250.vim
accents.vim                 esperanto.vim           kazakh-jcuken.vim            russian-jcukenmac.vim       slovak_iso-8859-2.vim
arabic.vim                  esperanto_utf-8.vim     lithuanian-baltic.vim        russian-jcukenwin.vim       slovak_utf-8.vim
arabic_utf-8.vim            greek.vim               magyar_utf-8.vim             russian-jcukenwintype.vim   tamil_tscii.vim
armenian-eastern_utf-8.vim  greek_cp1253.vim        mongolian_utf-8.vim          russian-yawerty.vim         thaana-phonetic_utf-8.vim
armenian-western_utf-8.vim  greek_cp737.vim         oldturkic-orkhon_utf-8.vim   serbian-latin.vim           thaana.vim
belarusian-jcuken.vim       greek_iso-8859-7.vim    oldturkic-yenisei_utf-8.vim  serbian-latin_utf-8.vim     ukrainian-dvorak.vim
bulgarian-bds.vim           greek_utf-8.vim         persian-iranian_utf-8.vim    serbian.vim                 ukrainian-jcuken.vim
bulgarian-phonetic.vim      hebrew.vim              persian.vim                  serbian_cp1250.vim          vietnamese-telex_utf-8.vim
canfr-win.vim               hebrew_cp1255.vim       pinyin.vim                   serbian_cp1251.vim          vietnamese-viqr_utf-8.vim
croatian.vim                hebrew_iso-8859-8.vim   polish-slash.vim             serbian_iso-8859-2.vim      vietnamese-vni_utf-8.vim
croatian_cp1250.vim         hebrew_utf-8.vim        polish-slash_cp1250.vim      serbian_iso-8859-5.vim
croatian_iso-8859-2.vim     hebrewp.vim             polish-slash_cp852.vim       serbian_utf-8.vim
croatian_utf-8.vim          hebrewp_cp1255.vim      polish-slash_iso-8859-2.vim  sinhala-phonetic_utf-8.vim
czech.vim                   hebrewp_iso-8859-8.vim  polish-slash_utf-8.vim       sinhala.vim
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/russian$ cat /usr/share/vim/vim81/keymap/NUGGET-TRAPPED 
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Gyre-Termes/Shapes
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/russian$ cd /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Gyre-Termes/Shapes
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Gyre-Termes/Shapes$ ls
DISPATCH  Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Gyre-Termes/Shapes$ cat DISPATCH 
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Script/Regular

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Gyre-Termes/Shapes$ cd /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Script/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Script/Regular$ ls -a
.  ..  .BLUEPRINT  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Script/Regular$ cat .BLUEPRINT 
Yahaha, you found me!
The next clue is in: /usr/share/icons/Adwaita/64x64/devices
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/Script/Regular$ cd /usr/share/icons/Adwaita/64x64/devices
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/64x64/devices$ ls
GIST                                    computer-symbolic.symbolic.png         modem-symbolic.symbolic.png
ac-adapter-symbolic.symbolic.png        drive-multidisk-symbolic.symbolic.png  printer-network-symbolic.symbolic.png
audio-headphones-symbolic.symbolic.png  input-dialpad-symbolic.symbolic.png    scanner-symbolic.symbolic.png
audio-headset-symbolic.symbolic.png     input-tablet-symbolic.symbolic.png
audio-speakers-symbolic.symbolic.png    media-removable-symbolic.symbolic.png
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/64x64/devices$ cat GIST
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{845yaut8BfJlaiu7Fqcrjizwljd.QX5IDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how to apply the 3 commands in this game using the hints given to obtain what is asked of us. 

### References 
None. 
