# LynxVE

This was an interesting one. I had to SSH into a server using the command `ssh ctf@lynxve.wpictf.xyz`,
using the password `lynxVE`

There I was shown a lynx Environment. It was showing a page of a CVS database. I was browsing the web using `G(o)`, 
when I suddenly realized "what if I can use `file:///home/`, doing so resulted in loading the home folder. Which showed the folder
`ctf` in `/home/` browsing to said folder showed the file `flag`. Which in turn on opening gave the flag 
`WPI{lynX_13_Gr8or_Th@n_Chr0m1Um}`. Entering this flag led to 50 points. Bringing our total points to 176.
