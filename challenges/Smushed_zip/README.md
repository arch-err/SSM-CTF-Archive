# Smushed_zip
*I had to scrape this zip file off the asphalt after someone ran it over, unfortunately i couldn't get it off in one piece.
*

## Solution
1. There are only five parts, so that would give us 5! permutations, but furst off, the easiest thing we could try is to just combine them in the given order (1-5).
2. The order 1-5 makes the dir-records look a bit weird, let's look at the parts individually with `zipdump.py`.
3. Alright, `part4` is definitely the DIR-records, and from these records we can figure out the order of the rest of the parts. The order is `5-3-1-2-4`. Combining these with the command `cat part5 part3 part1 part2 part4 > full.zip` gives us the real zip. Unzip it and get the flag...


## Flag
**Flag:** `SSM{y0u_un5mu5h3d_17}`
