Flag3 hint is 189*5 which gives you 945, where do you find numbers? Usually in the ID so if you go to the URL to ID and plug in that number
you'll find a flag. In this case, you go view a post and change the ID to 945 and you should get a flag.


![image](https://user-images.githubusercontent.com/113462727/194706331-5cc41fa8-8840-4c90-892d-9d679ce6c584.png)


![image](https://user-images.githubusercontent.com/113462727/194706363-f8ccb1b9-8716-4cd9-840d-647c94670229.png)


Flag4 hint -- you can change your own posts, can you change someone else's? There was a secret admin post in a previous flag. Let's go edit that. Go to edit one of your posts and change the url id to be 2. You'll have to actually edit the post and save it to get the flag.

![image](https://user-images.githubusercontent.com/113462727/194706498-e20b98c3-1ed4-4245-b2b0-a73db7638ca8.png)

There will be 2 flags, only because this page had a flag from a previous hint. You'll have to figure out which flag was correct and submit it.

![image](https://user-images.githubusercontent.com/113462727/194706560-dd27f474-571e-4199-91a5-d65c03e4a7bd.png)

Flag5 hint -- The cookie allows you to stay signed in. Can you figure out how they work so you can sign in to user with ID 1?

To get this, get a **cookie editor** extension for your browser. Both firefox and chrome have this in their extension stores. I went with **Cookie Editor** If you don't want to use an extension you can right click on the page > Inspect > Storage to get the cookie depending on the browser that might change, but either way the browser has a place already you can manipulate the cookie.

Got the cookie, looks like it could be a hash or encryption. 

![image](https://user-images.githubusercontent.com/113462727/194706937-41ead375-784e-45e9-bf36-8df263b4b1f0.png)


Sometimes throwing it in google will tell us the hash; Which it did comback as a MD5 Hash.

![image](https://user-images.githubusercontent.com/113462727/194707022-8a3a19ea-1b41-4fa9-9e7e-5622e7993d92.png)

We find the unhash is 3, which was the user id of our current user. Hash the number 1 (because we know that's the admin and that's what they gave us) as MD5, change that for the cookie and click on some action like write a post. Cyber Chef is usually good at doing this. 

NOTE: Don't forget to save the cookie as the new hash. It won't work if you don't.

Once the cookie is changed and saved, click home and you should get the following because you're now the admi and flag is at the top of the page.

![image](https://user-images.githubusercontent.com/113462727/194707549-d949570f-b9d9-4fe9-97a1-bc5cf1a6c9e5.png)

![image](https://user-images.githubusercontent.com/113462727/194707659-ddf1da97-bcaf-4a24-8c73-923e0f2ca64a.png)





