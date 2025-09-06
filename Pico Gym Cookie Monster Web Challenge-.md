To start off we are given a little bit of background with the challenge description being "Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?" I dont know about you but I hear a lot of cookies...
When we load the page this is what we see, ![[Desktop Screenshot 2025.09.06 - 10.04.40.07.png]]
I SEE A LOGIN, so ofc I try ' OR '1'='1 in both fields... It takes me to this page -
![[Desktop Screenshot 2025.09.06 - 10.06.21.16.png]]
Okay so its clear it has something to do with the cookies, lets go examine it...
[CTRL + I  Then Application Tab] -![[Desktop Screenshot 2025.09.06 - 10.08.26.72 1.png]]
So so our cookie looks a bit sus... Lets copy it and paste it into https://gchq.github.io/CyberChef/ 'cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzJDODA0MEVGfQ%3D%3D'
At first glance cyberchef doesn't pick anything up, and you might not either. But that ''%3D%3D" looks a little out of place, with a quick google search you can identify that its URL encoded and means == so our cookie is real base encoded. Lets go back to Cyberchef and change that %3D%3D to == and the magic feature should automatically pick it up, ![[Desktop Screenshot 2025.09.06 - 10.14.48.21.png]]
Nice it did, just hit the magic icon next to the 'Output' and that converts it to your flag!