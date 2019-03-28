# lession Linux

```
shadi@shadi-VirtualBox:~$ cd Desktop
shadi@shadi-VirtualBox:~/Desktop$ mkdir weekend
shadi@shadi-VirtualBox:~/Desktop$ cd weekend
shadi@shadi-VirtualBox:~/Desktop/weekend$ pwd
/home/shadi/Desktop/weekend
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo {A,b}{a,B,C}{1,2,3,&}.txt | tr ' ' '\n'
[1] 1904
Aa{1,2,3, AB{1,2,3, AC{1,2,3, ba{1,2,3, bB{1,2,3, bC{1,2,3,
}.txt: command not found
[1]+  Done                    echo {A,b}{a,B,C}{1,2,3,
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo {a..b}{1..6}.txt | tr ' ' '\n'
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo {a..b}{1..6}.txt | tr ' ' '\n'>text.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat text.txt
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo A$.txt >> text.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat text.txt
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ tree
.
└── text.txt

0 directories, 1 file
shadi@shadi-VirtualBox:~/Desktop/weekend$ mv text.txt test.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ tree
.
└── test.txt

0 directories, 1 file
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ whatis grep
grep (1)             - print lines matching a pattern
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep .2
a2.txt
b2.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep .txt
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -E "*"
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ clear

shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -E a
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep  a
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep  b
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep [a-b]
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ .[1-3]
.[1-3]: command not found
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep .[1-3]
a1.txt
a2.txt
a3.txt
b1.txt
b2.txt
b3.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep [1-3]
a1.txt
a2.txt
a3.txt
b1.txt
b2.txt
b3.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep a1
a1.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -A1 a1
a1.txt
a2.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -A2 a1
a1.txt
a2.txt
a3.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -B2 a1
a1.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -B2 b1
a5.txt
a6.txt
b1.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -C2 b1
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -C2 b2
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ clear

shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep [^1-4]
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | grep -E [^1-4]
a1.txt
a2.txt
a3.txt
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ whatis tail
tail (1)             - output the last part of files
shadi@shadi-VirtualBox:~/Desktop/weekend$ man tail
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | tail
a4.txt
a5.txt
a6.txt
b1.txt
b2.txt
b3.txt
b4.txt
b5.txt
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | tail -n2
b6.txt
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | head -n2
a1.txt
a2.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | head -n5 | tail -n2
a4.txt
a5.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt | head -n8 | tail -n2 
b1.txt
b2.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ whatis cut
cut (1)              - remove sections from each line of files
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0<div class="Translation_divMiddle_enTohe">
        <div class="normal_translation_div">
כֶּלֶב<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) בָּחוּר, בַּרְנָשׁ<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) אדם נבזה<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה        </div>
--
<div class="Translation_divMiddle_enTohe">
        <div class="normal_translation_div">
רָדַף<span class='clearOutputLanguageMeaningsString'>; </span>הִטְרִיד        </div>
100  206k  100  206k    0     0   172k      0  0:00:01  0:00:01 --:--:--  172k
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -A1 normal_translation_div | head -n2
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  206k  100  206k    0     0   193k      0  0:00:01  0:00:01 --:--:--  193k
        <div class="normal_translation_div">
כֶּלֶב<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) בָּחוּר, בַּרְנָשׁ<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) אדם נבזה<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -A1 normal_translation_div | head -n2 | tail 1
tail: cannot open '1' for reading: No such file or directory
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  204k  100  204k    0     0   228k      0 --:--:-- --:--:-- --:--:--  227k
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -A1 normal_translation_div | head -n2 | tail -n1
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  206k  100  206k    0     0   203k      0  0:00:01  0:00:01 --:--:--  203k
כֶּלֶב<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) בָּחוּר, בַּרְנָשׁ<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) אדם נבזה<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -A1 normal_translation_div | head -n2 | tail -n1
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--    100  189k  100  189k    0     0  83991      0  0:00:02  0:00:02 --:--:-- 83991
חָתוּל        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -A1 normal_translation_div | head -n2 | tail -n1 >> a.txt
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     50  189k   50 97299    0     0  99793      0  0:00:01 --:--:--  0:00:01 996100  189k  100  189k    0     0   181k      0  0:00:01  0:00:01 --:--:--  181k
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat a.txt
חָתוּל        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -A1 normal_translation_div | head -n2 | tail -n1 | tr 'div' ''
tr: when not truncating set1, string2 must be non-empty
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     23  204k   23 48147    0     0  54526      0  0:00:03 --:--:--  0:00:03 544100  204k  100  204k    0     0   185k      0  0:00:01  0:00:01 --:--:--  185k
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -C1 normal_translation_div | head -n3 | tr '<div/' ' '
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  189k  100  189k    0     0   149k      0  0:00:01  0:00:01 --:--:--  149k
     class="Translat on_   M   le_enTohe">
             class="normal_translat on_   ">
חָתוּל             >
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -C1 normal_translation_div | head -n3 | tr '<div/>' ' '
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     84  189k   84  159k    0     0  69660      0  0:00:02  0:00:02 --:--:-- 696100  189k  100  189k    0     0  82034      0  0:00:02  0:00:02 --:--:-- 82000
     class="Translat on_   M   le_enTohe" 
             class="normal_translat on_   " 
חָתוּל              
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -C1 normal_translation_div | head -n3 | tail -n1  | tr '<div/>' ' '
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  189k  100  189k    0     0   181k      0  0:00:01  0:00:01 --:--:--  181k
חָתוּל shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/cat | grep -C1 normal_translation_div | head -n3 | tail -n1  | tr '<div/>' ' ' | rev
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  191k  100  191k    0     0   186k      0  0:00:01  0:00:01 --:--:--  186k
              לּותָחshadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div | tr '<div/>' ' ' 
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  204k  100  204k    0     0   137k      0  0:00:01  0:00:01 --:--:--  137k
     class="Translat on_   M   le_enTohe" 
             class="normal_translat on_   " 
כֶּלֶב span class='clearOutputLanguageMean ngsStr ng' ;   span (בלשון הדיבור) בָּחוּר, בַּרְנָשׁ span class='clearOutputLanguageMean ngsStr ng' ;   span (בלשון הדיבור) אדם נבזה span class='clearOutputLanguageMean ngsStr ng' ;   span (בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה              
--
     class="Translat on_   M   le_enTohe" 
             class="normal_translat on_   " 
רָדַף span class='clearOutputLanguageMean ngsStr ng' ;   span הִטְרִיד              
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div | head -n3
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  204k  100  204k    0     0   168k      0  0:00:01  0:00:01 --:--:--  168k
<div class="Translation_divMiddle_enTohe">
        <div class="normal_translation_div">
כֶּלֶב<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) בָּחוּר, בַּרְנָשׁ<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) אדם נבזה<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div | head -n3 | tail -n1
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  206k  100  206k    0     0   167k      0  0:00:01  0:00:01 --:--:--  167k
כֶּלֶב<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) בָּחוּר, בַּרְנָשׁ<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) אדם נבזה<span class='clearOutputLanguageMeaningsString'>; </span>(בלשון הדיבור) עַל הַפָּנִים, תַּת-רָמָה        </div>
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div | head -n3 | tail -n1 | rev
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  204k  100  204k    0     0   181k      0  0:00:01  0:00:01 --:--:--  182k
>vid/<        הָמָר-תַּת ,םיִנָּפַה לַע )רובידה ןושלב(>naps/< ;>'gnirtSsgninaeMegaugnaLtuptuOraelc'=ssalc naps<הזבנ םדא )רובידה ןושלב(>naps/< ;>'gnirtSsgninaeMegaugnaLtuptuOraelc'=ssalc naps<ׁשָנְרַּב ,רּוחָּב )רובידה ןושלב(>naps/< ;>'gnirtSsgninaeMegaugnaLtuptuOraelc'=ssalc naps<בֶלֶּכ
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://www.morfix.co.il/dog | grep -C1 normal_translation_div | head -n3 | tail -n1 | cut -d "<" -f 1 | rev
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  206k  100  206k    0     0   193k      0  0:00:01  0:00:01 --:--:--  193k
בֶלֶּכ


```
