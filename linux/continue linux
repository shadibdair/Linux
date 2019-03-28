# continue linux regex
```
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
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt  | grep '^[[:lower:]]'
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
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAa" | grep a
aAa
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAab" | grep ab
aAab
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAab" | grep '^ab
> bash: unexpected EOF while looking for matching `''
bash: syntax error: unexpected end of file
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAab" | grep '^ab'
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAab" | grep 'ab'
aAab
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAab" | grep 'ab$'
aAab
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAaba" | grep 'ab$'
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "aAaba" | grep '^A'
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt  | grep '^A'
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ cat test.txt  | grep '^A\$'
A$.txt
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "shadi@gmail" | grep '.'
shadi@gmail
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "shadi@gmail" | grep '\.'
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo {1..4}
1 2 3 4
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo [1-4]
[1-4]
shadi@shadi-VirtualBox:~/Desktop/weekend$ echo "shadi@gmail" | grep {1..4}
grep: 2: No such file or directory
grep: 3: No such file or directory
grep: 4: No such file or directory
shadi@shadi-VirtualBox:~/Desktop/weekend$ cd ..
shadi@shadi-VirtualBox:~/Desktop/linux$ cd ..
shadi@shadi-VirtualBox:~/Desktop$ ls -l
total 12
-rw-r--r-- 1 shadi shadi 1288 Mar 28 18:56 'continue linux'
drwxrwxr-x 3 shadi shadi 4096 Mar 28 18:33  linux
drwxrwxr-x 2 shadi shadi 4096 Mar 26 12:59  scapy
shadi@shadi-VirtualBox:~/Desktop$ ls -l | grep '^-'
-rw-r--r-- 1 shadi shadi 1288 Mar 28 18:56 continue linux
shadi@shadi-VirtualBox:~/Desktop$ ls -l | grep '^d'
drwxrwxr-x 3 shadi shadi 4096 Mar 28 18:33 linux
drwxrwxr-x 2 shadi shadi 4096 Mar 26 12:59 scapy
shadi@shadi-VirtualBox:~/Desktop$ ls -l | grep '^.....-'
-rw-r--r-- 1 shadi shadi 1288 Mar 28 18:56 continue linux
shadi@shadi-VirtualBox:~/Desktop$ ls -l | grep '[1-24-7]'
total 12
-rw-r--r-- 1 shadi shadi 2272 Mar 28 19:03 continue linux
drwxrwxr-x 3 shadi shadi 4096 Mar 28 18:33 linux
drwxrwxr-x 2 shadi shadi 4096 Mar 26 12:59 scapy

```
