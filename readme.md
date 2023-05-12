# Challenges

Sovlving some challenges

## FTP

Open the file `ch1.pcap` (donwloaded on the website) in Wireshark.
Hit on button Analyser (on the top)
Then, Hit on the button `Follow`.
Then click on `TCP`

The password is on the line where there is pass : *******

---

## TELNET

Open the file `ch2.pcap` (downloaded on the website) in Wireshark.
Hit on button Analyser (on the top)
Then, Hit on the button `Follow`.
Then click on `TCP`

The password is on the line where there is Password : *******

---

## Twitter Authentification

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

## ETHERNET Trame

---

## BLUETOOTH
