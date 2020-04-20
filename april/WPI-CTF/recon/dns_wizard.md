# dns_wizard

This was a bit of a hard one, as we had no idea how `nslookup` worked, though we knew it existed.

As we could guess from the title it had to do with DNS queries. Thus we went googling for DNS lookup sites 
(because we couldn't be arsed to use `nslookup`). Using the fact we weren't given info on what site to use, we directly used
`wpictf.xyz` as input for the lookup query. There we were shown a TXT record with base64 encoding.

This TXT record was the string `V1BJezFGMHVuZF9UaDNfRE5TLXJlY29yZH0=`

Decoding the base64 encoded text using [base64decode.org](https://www.base64decode.org/) led to the flag.

The flag was: `WPI{1F0und_Th3_DNS-record}`

Entering it led to **50** points bringing our total to **101** points.
