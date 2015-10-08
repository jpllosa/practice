thank you for reading.
burn after reading.
save after burning.
one more fetch and merge.
fetch and then merge is equal to a pull.
so, you git pull <URL> to update your local files.
modify your files.
then you git add files.
next you git commit -am "meaningful message for this commit"
lastly git push <URL>
you can get the <URL> by copy and paste from github.com clone url option
how to do the issue thing in git?
start an issue via github.com
close an issure by adding "Closes #<issue number>" in the commit message.

readme already reaches column number 70 with line number 11 and 14.  in
fact, they even passed it.

what shall we practice today?  we have tried issue.  let try the command
git blame README.txt
here is the output
$ git blame README.txt
a7c17035 (jpllosa 2015-09-01 22:50:03 +0800  1) thank you for reading.
a7c17035 (jpllosa 2015-09-01 22:50:03 +0800  2) burn after reading.
a923d832 (jpllosa 2015-09-01 23:01:08 +0800  3) save after burning.
d037af2c (jpllosa 2015-09-01 23:09:15 +0800  4) one more fetch and merge.
95cde9fd (jpllosa 2015-09-05 01:24:37 +0800  5) fetch and then merge is equal to
5c714654 (jpllosa 2015-09-08 22:02:23 +0800  6) so, you git pull <URL> to update
7203946d (jpllosa 2015-09-08 22:22:05 +0800  7) modify your files.
66b88531 (jpllosa 2015-09-08 22:18:13 +0800  8) then you git add files.
7203946d (jpllosa 2015-09-08 22:22:05 +0800  9) next you git commit -am "meaning
7203946d (jpllosa 2015-09-08 22:22:05 +0800 10) lastly git push <URL>
6b3c4a21 (jpllosa 2015-09-24 16:39:23 +0800 11) you can get the <URL> by copy an
6b3c4a21 (jpllosa 2015-09-24 16:39:23 +0800 12) how to do the issue thing in git
ebdf1d47 (jpllosa 2015-09-17 12:31:15 +0800 13) start an issue via github.com
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 14) close an issure by adding "Close
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 15)
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 16) readme already reaches column nu
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 17) fact, they even passed it.

okay, so we know who committed and when.  even further let's try
git blame -L 10, 15 REAMDME.txt

$ git blame -L 10,15 README.txt
7203946d (jpllosa 2015-09-08 22:22:05 +0800 10) lastly git push <URL>
6b3c4a21 (jpllosa 2015-09-24 16:39:23 +0800 11) you can get the <URL> by copy an
6b3c4a21 (jpllosa 2015-09-24 16:39:23 +0800 12) how to do the issue thing in git
ebdf1d47 (jpllosa 2015-09-17 12:31:15 +0800 13) start an issue via github.com
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 14) close an issure by adding "Close
aa7638ac (jpllosa 2015-09-24 22:18:35 +0800 15)

ah, okay, this shows who committed and when but within the scope
of -L 10,15 which is line/commit 10 to 15
