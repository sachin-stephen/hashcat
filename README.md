# hashcat
*Download dictionary*

![image](https://user-images.githubusercontent.com/111299090/196280043-23269363-e50d-4c65-b177-9e140c47aaa7.png)

*Uncompress the dictionary file using the below command*

┌──(kali㉿kali)-[~]
└─$ 
```bash
gzip -d crackstation.txt.gz   
```
```Use manual to use the hashcat to decrypt the hashes```<br />

```Check @hash types for the hash mode value```<br />

```check dictionary path```<br />

```pwd```   ```ls```     ```cd```

```bash
cd /home/kali/Downloads/crackstation.txt
```

┌──(kali㉿kali)-[~]
└─$ 
```bash
hashcat -m 3200 "\$2y\$12\$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom" /home/kali/Downloads/crackstation.txt
```
```bash
hashcat (v6.2.5) starting

OpenCL API (OpenCL 1.2 pocl 1.6, None+Asserts, LLVM 9.0.1, RELOC, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
=============================================================================================================================
* Device #1: pthread-Intel(R) Core(TM) i5-9300H CPU @ 2.40GHz, 1370/2805 MB (512 MB allocatable), 2MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 72

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Single-Hash
* Single-Salt

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 0 MB

Dictionary cache building /home/kali/Downloads/crackstation.txt: 100660338 bytes (0.64%

Dictionary cache built:
* Filename..: /home/kali/Downloads/crackstation.txt
* Passwords.: 1212356398
* Bytes.....: 15696118781
* Keyspace..: 1212336035
* Runtime...: 5 mins, 18 secs
```
```bash
[s]tatus [p]ause [b]ypass [c]heckpoint [f]inish [q]uit => s

Session..........: hashcat
Status...........: Running
Hash.Mode........: 3200 (bcrypt $2*$, Blowfish (Unix))
Hash.Target......: $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX...8wsRom
Time.Started.....: Mon Oct 17 15:30:27 2022 (48 secs)
Time.Estimated...: Sat May 13 05:17:00 2045 (22 years, 208 days)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (/home/kali/Downloads/crackstation.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:        2 H/s (3.51ms) @ Accel:2 Loops:16 Thr:1 Vec:1
Recovered........: 0/1 (0.00%) Digests
Progress.........: 80/1212336035 (0.00%)
Rejected.........: 0/80 (0.00%)
Restore.Point....: 80/1212336035 (0.00%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:416-432
Candidate.Engine.: Device Generator
Candidates.#1....: ``_ -> ``-
Hardware.Mon.#1..: Util: 91%
```


