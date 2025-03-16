# Zaknas
*Jag zippade ihop några bilder jag tagit, men när jag öppnar zippen så verkar en bild zaknas. Jag kan svära på att bilden fortfarande finns där inne...*

## Solution
1. Hmm.... Interesting! So, we're given a zip archive where a file doesn't get extracted with unzip. The reason for this is that there are no DIR-records (you can inspect this with the command `zipdump.py -f l zaknas.zip`).
2. In theory we could get the offset of the file before the flag, then add the size of that file to get the offset of the flag-file. Then we just get the offset for the file after it, and then carve out the flag in between those offsets. A way easier approach would just be to use `zipdump.py` though.
3. `zipdump.py -f 0x0003be4b -s decompress -d zaknas.zip > flag.zip && unar flag.zip && rm flag.zip`
4. So, according to the flag contents you probably couldve used `binwalk` to solve this too...


## Flag
**Flag:** `SSM{zn34ky_zn34ky_b1nw4lk_l34ky}`
