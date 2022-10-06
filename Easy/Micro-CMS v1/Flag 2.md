
Full explanation for this found on [Michael W. Norris](https://mnorris.io/hackerone%20ctf/h1_Micro-CMS_v1/) but I want to credit this person because it took me forever to understand how this worked, even a year or so later. I'll paraphrase here, but check his page for more information.

We start off here again.

![image](https://user-images.githubusercontent.com/113462727/194408464-c82faf0d-ed36-4557-bb6e-5a7a99603401.png)




If you go to the edit page and throw a single quote in the URL, you'll find that it gives you the flag.

![image](https://user-images.githubusercontent.com/113462727/194416223-ca024bf2-030f-45f3-a778-293774c32a71.png)



Apparently this works because the developer didn't use any type of input validation/sanitization. It's unexpected behavior that wasn't handled. It would've thrown an error but it threw us a flag :)

![image](https://user-images.githubusercontent.com/113462727/194416562-a9622a54-2866-4b78-a8a5-56ed5bbc4f5e.png)

