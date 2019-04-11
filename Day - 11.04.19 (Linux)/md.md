# linux -- egrep--
```
shadi@shadi-VirtualBox:~$ echo "aa"  | egrep a{2}
aa
shadi@shadi-VirtualBox:~$ echo "aa"  | grep  "a\{2\}"
aa
shadi@shadi-VirtualBox:~$ echo "aa"  | egrep  "a{2}"
aa
shadi@shadi-VirtualBox:~$ cat > a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ cat  a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ grep "bale" a.txt
gareth bale 32 bbbb
shadi@shadi-VirtualBox:~$ cat a.txt| grep "bale"
gareth bale 32 bbbb
shadi@shadi-VirtualBox:~$ cat a.txt| grep -o "bale"
bale

shadi@shadi-VirtualBox:~$ egrep [s-G4-6] a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep [s-G2-6] a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep ^[a-z] a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep ^[^a-z] a.txt
shadi@shadi-VirtualBox:~$ egrep ^[^x-z] a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep ^[^sb] a.txt
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep n a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep n$ a.txt
shadi@shadi-VirtualBox:~$ egrep o$ a.txt
shadi@shadi-VirtualBox:~$ egrep c$ a.txt
cristiano ronaldo 30 cccc
hadi@shadi-VirtualBox:~$ egrep ^c$ a.txt  // seraching for only c
shadi@shadi-VirtualBox:~$ egrep ^.r a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "^.{5}i" a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ echo "aaaaaaa" | egrep "^a*$"
aaaaaaa
shadi@shadi-VirtualBox:~$ echo "1a5" | egrep "^[1-5]a*[1-5]$"
1a5
shadi@shadi-VirtualBox:~$ echo "1a5" | egrep "^[1-5]a+[1-5]$"
1a5
shadi@shadi-VirtualBox:~$ echo "15" | egrep "^[1-5]a+[1-5]$"
shadi@shadi-VirtualBox:~$ echo "1aaa5" | egrep "^[1-5]a{2,7}[1-5]$"
1aaa5
shadi@shadi-VirtualBox:~$ egrep "^.r" a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "^.?r" a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "^.c?r" a.txt
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep s  a.txt
shadi bdair 20 aaaa
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "[a-z]{1,}"  a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "." a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "(.)\1" a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ egrep "(.)\1$" a.txt
shadi bdair 20 aaaa
gareth bale 32 bbbb
cristiano ronaldo 30 cccc
shadi@shadi-VirtualBox:~$ echo "123321" | egrep "(.)(.)(.)\3\2\1"
123321
shadi@shadi-VirtualBox:~$ echo "abccba" | egrep "(.)(.)(.)\3\2\1"
abccba
shadi@shadi-VirtualBox:~$ echo "12" | egrep "([1-5])([1-5])"
12
shadi@shadi-VirtualBox:~$ echo "12" | egrep "([1-5])\1"
shadi@shadi-VirtualBox:~$ echo "22" | egrep "([1-5])\1"
22
shadi@shadi-VirtualBox:~$ echo "ababa" | egrep "^((.).)\1\2$"
ababa
shadi@shadi-VirtualBox:~$ ls -l | wc
     24     210    1239
shadi@shadi-VirtualBox:~$ echo "abc" | wc
      1       1       4
shadi@shadi-VirtualBox:~$ echo "abc " | wc
      1       1       5
shadi@shadi-VirtualBox:~$ echo "abc dse" | wc
      1       2       8
shadi@shadi-VirtualBox:~$ echo "abc dse" | wc -l
1
shadi@shadi-VirtualBox:~$ echo $(ls) 
app1.py app.py a.txt CaptureFile.cap CaptureFile.pcap Desktop Documents Downloads examples.desktop linux Day_28.03.19 list.txt Music Pictures Public readd_test.py read_test.py send_test.py snap Templates test_pcap test.pcap text.txt Videos
shadi@shadi-VirtualBox:~$ echo [1+1]
[1+1]
shadi@shadi-VirtualBox:~$ echo $[1+1]
2
shadi@shadi-VirtualBox:~$ echo $[$(echo 2)+1]
3
shadi@shadi-VirtualBox:~$ curl https//jsonplaceholder.typicode.com/todos
curl: (6) Could not resolve host: https
shadi@shadi-VirtualBox:~$ sudo apt install jq
shadi@shadi-VirtualBox:~$ curl https://jsonplaceholder.typicode.com/todos

```
---
```
shadi@shadi-VirtualBox:~$ uptime
 17:26:03 up  1:16,  1 user,  load average: 0.00, 0.06, 0.08
shadi@shadi-VirtualBox:~$ uptime -s
2019-04-11 16:09:19

shadi@shadi-VirtualBox:~$ lscpu
Architecture:        x86_64
CPU op-mode(s):      32-bit, 64-bit
Byte Order:          Little Endian
CPU(s):              1
On-line CPU(s) list: 0
Thread(s) per core:  1
Core(s) per socket:  1
Socket(s):           1
NUMA node(s):        1
Vendor ID:           GenuineIntel
CPU family:          6
Model:               142
Model name:          Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz
Stepping:            9
CPU MHz:             2712.000
BogoMIPS:            5424.00
Hypervisor vendor:   KVM
Virtualization type: full
L1d cache:           32K
L1i cache:           32K
L2 cache:            256K
L3 cache:            3072K
NUMA node0 CPU(s):   0
Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_freq pni pclmulqdq monitor ssse3 cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase avx2 invpcid rdseed clflushopt
```

---
#### you have this
```
shadi@shadi-VirtualBox:~$ lscpu -J | jq
{
  "lscpu": [
    {
      "field": "Architecture:",
      "data": "x86_64"
    },
    {
      "field": "CPU op-mode(s):",
      "data": "32-bit, 64-bit"
    },
    {
      "field": "Byte Order:",
      "data": "Little Endian"
    },
    {
      "field": "CPU(s):",
      "data": "1"
    },
    {
      "field": "On-line CPU(s) list:",
      "data": "0"
    },
    {
      "field": "Thread(s) per core:",
      "data": "1"
    },
    {
      "field": "Core(s) per socket:",
      "data": "1"
    },
    {
      "field": "Socket(s):",
      "data": "1"
    },
    {
      "field": "NUMA node(s):",
      "data": "1"
    },
    {
      "field": "Vendor ID:",
      "data": "GenuineIntel"
    },
    {
      "field": "CPU family:",
      "data": "6"
    },
    {
      "field": "Model:",
      "data": "142"
    },
    {
      "field": "Model name:",
      "data": "Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz"
    },
    {
      "field": "Stepping:",
      "data": "9"
    },
    {
      "field": "CPU MHz:",
      "data": "2712.000"
    },
    {
      "field": "BogoMIPS:",
      "data": "5424.00"
    },
    {
      "field": "Hypervisor vendor:",
      "data": "KVM"
    },
    {
      "field": "Virtualization type:",
      "data": "full"
    },
    {
      "field": "L1d cache:",
      "data": "32K"
    },
    {
      "field": "L1i cache:",
      "data": "32K"
    },
    {
      "field": "L2 cache:",
      "data": "256K"
    },
    {
      "field": "L3 cache:",
      "data": "3072K"
    },
    {
      "field": "NUMA node0 CPU(s):",
      "data": "0"
    },
    {
      "field": "Flags:",
      "data": "fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_freq pni pclmulqdq monitor ssse3 cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase avx2 invpcid rdseed clflushopt"
    }
  ]
}

```

### get where you have "field" 
#### the result --> lscpu -J | jq '.lscpu[].''field'
```
shadi@shadi-VirtualBox:~$ lscpu -J | jq '.lscpu[].''field'
"Architecture:"
"CPU op-mode(s):"
"Byte Order:"
"CPU(s):"
"On-line CPU(s) list:"
"Thread(s) per core:"
"Core(s) per socket:"
"Socket(s):"
"NUMA node(s):"
"Vendor ID:"
"CPU family:"
"Model:"
"Model name:"
"Stepping:"
"CPU MHz:"
"BogoMIPS:"
"Hypervisor vendor:"
"Virtualization type:"
"L1d cache:"
"L1i cache:"
"L2 cache:"
"L3 cache:"
"NUMA node0 CPU(s):"
"Flags:"

```