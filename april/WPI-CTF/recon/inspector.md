# Inspector

This was a bit of a tricky one, even though it would give **25** points. As we got tricked into looking in the wrong direction.

With the fact that the text said the flag would possibly be on the CTF's site, we went to use our knowledge of earlier CTFs.

As such, we went to visit the mainpage using inspect element, over at [WPICTF](https://wpictf.xyz/)
This gave a confirmation to our suspicion that there would be anotherhint in `robots.txt`.

Visiting the [robots.txt](https://wpictf.xyz/robots.txt) file led to the file `inspector.txt` on the same site.

Looking at said file, we forgot that it would be on the same site we were looking at. Anyway, after googling we came across
[the CSC's site](https://web.cs.wpi.edu/~csc/).

Inspecting the element there gave a commented out base64encoded string:
`VGhpcyBzaXRlIGlzIHB1cmVseSBpbmZvcm1hdGlvbi4gQnV0IHdlIGFwcHJlY2lhdGUgdGhlIGVmZm9ydCBkZWNvZGluZyB0aGlzLg==`

Decoding that using [base64decode](https://base64decode.org) we got as text:
"This site is purely information. But we appreciate the effort decoding this."

Annoyed by it, we tried to enter the `WPI{FLAG}` comment we found before visiting robots.txt until we saw twice that it failed.

Then we went back to what possibly went wrong. Then we realized it was on the same site, namely the subdomain:
[ctf.wpictf.xyz](https://ctf.wpictf.xyz/)

Looking through it, we thought: why not look through some pages on the site.

Then at the [prizes page](https://ctf.wpictf.xyz/prizes) we found the flag.

The flag was: `WPI{1nsp3ct0r_H@ck3R}`

This gave us **25** points, which brought our total to **126** points.
