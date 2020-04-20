# LynxVE

This was an interesting one. We had to SSH into a server using the command `ssh ctf@lynxve.wpictf.xyz`
where the password was `lynxVE`

There we were shown a lynx Environment. It was showing a page of a CVS database. We started browsing the web using `G(o)`, 
when we suddenly realized "what if we can use `file:///home/`".

When we did that, we were shown the contents of the `/home/` folder, this gave us the home folder of the user `ctf` in `/home/`.

After browsing to said folder we were shown the file `flag`.

After opening this file, we were shown the flag, which was: `WPI{lynX_13_Gr8or_Th@n_Chr0m1Um}`. 

Entering this flag led to **50** points. Bringing our total points to **176**.
