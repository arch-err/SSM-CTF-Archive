# Tangentbord
*Vi hittade ett tangentbord med texten "ultimate speed" skrivet på sidan och kopplade in det, men det verkar inte riktigt fungera som det ska...*

`ssh ctf@188.126.67.132 -p 40109`
`ctf:Vhbmhkbk91o6wams`

## Solution
1. `sshpass -p Vhbmhkbk91o6wams ssh ctf@188.126.67.132 -p 40109`
2. Just try keys until you find `c` (`i`), `a` (`a`), `t` (`k`), `.` (`z`). We can use this together with `/`, `*`, and `?`. Then we can ***type*** strings like `iak /???/???/z*`, which will match `/etc/X11/.Xauthority`
3. Looking around the files and following leads will give you the flag.


## Flag
**Flag:** `cratectf{dvorak_gets_better_with_practice}`
