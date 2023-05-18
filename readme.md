# Challenges

Sovlving some challenges

## FTP

Open the file `ch1.pcap` (donwloaded on the website) in Wireshark.

Hit on button Analyser (on the top).

Then, Hit on the button `Follow`.

Then click on `TCP flux`

The password is on the line where there is pass : *******

---

## TELNET

Open the file `ch2.pcap` (downloaded on the website) in Wireshark.
Hit on button Analyser (on the top).

Then, Hit on the button `Follow`.

Then click on `TCP flux`

The password is on the line where there is Password : *******

---

## Twitter Authentification

Open the file `ch4.pcap` (downloaded on the website) in Wireshark.

Hit the button `Analyser` (on the top).

Then, Hit on the button `Follow`.

Then click on `TCP flux`

```cmd
GET /statuses/replies.xml HTTP/1.1
User-Agent: CFNetwork/330
Cookie: _twitter_sess=BAh7CDoJdXNlcjA6B2lkIiVmZGQ2ODc5MTMwMWFhOTFiMWExZDViZmQwMGEz%250AOWNkMyIKZmxhc2hJQzonQWN0aW9uQ29udHJvbGxlcjo6Rmxhc2g6OkZsYXNo%250ASGFzaHsABjoKQHVzZWR7AA%253D%253D--ea12e7bc090d05202cd7e3f972c2b4414a97f657
Accept: */*
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Authorization: Basic dXNlcnRlc3Q6cGFzc3dvcmQ=
Connection: keep-alive
Host: twitter.com
```

decode the base64 data on line that have **Authorization** :
dXNlcnRlc3Q6cGFzc3dvcmQ= on [RapidTable](https://www.rapidtables.com/web/tools/base64-decode.html)

Then you got the decoded password after usertest:*****

---

## ETHERNET Trame

Get to [HexDecode](https://www.convertstring.com/fr/EncodeDecode/HexDecode) and paste the Hexadecimal data from file `ch3.txt` (downloaded on the site)
Then decode it.

We got this :

```cmd
�s ��àiØZÝ`����@&S��`*¼����ºÞÀÞ AÐ�B3�������t�P¼ê}¸�Á×�áÏ ��
>i¹¡~ÓGET / HTTP/1.1
Authorization: Basic Y29uZmk6ZGVudGlhbA==
User-Agent: InsaneBrowser
Host: www.myipv6.org
Accept: */*
```

There is base64 data on the line `Authorization: Basic .....`, because it has **alphanumeric characters**

Copy the base64 data from the line where there is `Authorisation` : **Y29uZmk6ZGVudGlhbA==** and decode it on [RapidTable](https://www.rapidtables.com/web/tools/base64-decode.html)

Then, we get the password

---

## BLUETOOTH

Open the file `ch18.bin` (downloaded on the website) in Wireshark.

Hit the button `Wireless` (on the top).

The click on the button `Bluetooth devices`.

concatenate the Mac address and the name : 0C:B3:19:B9:4F:C6GT-S7390G.

Then, hash it to SHA1 encoding on [SHA1](https://www.sha1.fr/) and you get the password.

## SSL - échange HTTP

open file `ch5.pcap` from the challenge in Wireshark.

Then with the hint : "google is your friend : inurl:server.pem...", let's get search
in google and we may get first to this [bad url](https://github.com/fuzyll/defcon-vm/blob/master/extras/hfd/server.pem); but we need is on [This one](https://raw.githubusercontent.com/Hypernode/M2Crypto/master/demo/x509/server-expired.pem).

the content file is like [this](./server.pem).

Then, save the `RSA private key part` in a new file like **rsa.pem** for example.

After, go to Wireshark preference and add the `rsa.pem` to rsa key

then click on ANALYSER button and follow the flux tls.

You get the password

twisted by design
