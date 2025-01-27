# aurora_pico
picoctf challenges for aurora
1. Inspect HTML
we click inspect on the website and then we find the flag within the tags

2. IntroToBurp
download burpsuite community edition
open chromium browser
and copy paste the url for the registration details
fill in test in all fields including otp and then open burpsuite
inside proxy open http history and then post /dashboard is the last request we sent click on that
right click send to repeater
and then open repeater we can render do garbage=test instead of otp=test
flag = picoCTF{#0TP_Bypvss_SuCc3$S_b3fa4f1a}

3. dont use client side
password in form of js string
flag = picoCTF{no_clients_plz_1a3c89}

4.where are the robots
so robots.txt is used to specify parts of the website which can or can not be accessed by the automated agents
so in the url we add robots.txt
we know the disallowed part exists in the page so we add that in the url which gives us the flag
flag = picoCTF{ca1cu1at1ng_Mach1n3s_8028f}

5.SQL Direct
we use the webshell and connect to postgresql
and then using the basic commands in the flag table we find the flag
flag = picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
\list
\c pico
\dt
\d flags
select * from flags

6.some assembly required 1
we inspect and go to sources and then wasm and we find the flag 
flag= picoCTF{d88090e679c48f3945fcaa6a7d6d70c5}

7.some assembly required 2
in the wasm file we find a file that is encrypted which we must decrypt so we find that i32 xor is being carried out so we decrypt using https://www.dcode.fr/xor-cipher and using brute force we find the flag 
flag= picoCTF{b2d14eaec72c31305075876bff2b5d}

8.some assembly required 3
cant install wabt

9. who are you
keep intercept off initially
then change user agent to PicoBrowser
Referer:mercury...
Date:2018
X-Forwaded-For:103.103.84.0
Accept-Language:sv


10.power cookie
change value of cookie to 1 
flag = picoCTF{gr4d3_A_c00k13_5d2505be}
