This challenge is titled 'IntroToBurp' so its safe to assume we will be using BurpSuite, MY FAVORITE!!

Anyways, when we go to the given link we are asked for alot of information. I started by opening up my Community Edition Burp Suite and navigating to the proxy tab, from this we will open our browser and paste the challenge link. Once we are on that register page were gonna want to turn on that intercept in proxy.

I chose to just put 'test' in all the places it asked for information, after sending the request it will be stopped in the proxy until you send it to repeater and forward it. After that we will do the same thing with the 2fa authentication, I sent 'test' and sent that request to the repeater.

Now lets go to our repeater and send all the requests, you'll want to examine most of them to see if theres something hidden. Upon first glance at the sent requests I noticed the 2nd one (or the 2fa auth) was a GET request, where as all the others were POST... So I changed it to a POST req and sent it, BOOM theres the flag! 

"Welcome, test you sucessfully bypassed the OTP request. 
Your Flag: picoCTF{#0TP_Bypvss_SuCc3$S_9090d63c}"

But I cheated it, in the reponse of that original request it shows.

```  
<form method="POST">
<input type="text" name="otp" placeholder="Enter OTP">
<button type="submit">      
```

Ahhhh, so thats where it shows us we need it to be post!

