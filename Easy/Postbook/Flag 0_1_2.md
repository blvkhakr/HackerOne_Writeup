Alright so I broke down and decided to do index starting at 0. Here you'll find the first three flags for Postbook.


![Screenshot from 2022-10-08 20-22-15](https://user-images.githubusercontent.com/113462727/194704976-f1e237a2-3da5-4b91-9039-c9a7df80c10d.png)


First flag is pretty easy. The hint tells us that the creds are **user/password** so click on Sign in and use the creds

![image](https://user-images.githubusercontent.com/113462727/194705022-12b4f703-48c4-412b-9767-2cf117d8287a.png)


![image](https://user-images.githubusercontent.com/113462727/194705069-f316b61b-80de-485b-994d-d80125a53150.png)


Flag1 tells us that we should try viewing our own post and see if we can change the ID. I decided to sign up and get a flag this way. It helps going back for me. so I create a user.

![image](https://user-images.githubusercontent.com/113462727/194705280-eff388d9-a10b-4f3e-b306-a0a5eb4470f1.png)


From there, I create a post and edit that post. Check out the URL of that post to see there is an ID
![image](https://user-images.githubusercontent.com/113462727/194705471-0df60a44-7154-4ef6-ad59-89cc99ee421b.png)


Notice that you have to go to **Write a New post** to get this flag, it doesn't work any other way.

![image](https://user-images.githubusercontent.com/113462727/194705526-50fdfc36-1fbb-46c8-a23b-84ad4a97233d.png)

Check out the URL that says **view.php&success=1&id=6&message** Change the ID to be something else until you get a flag. In this case, it was **id=2** this might change for you.

![image](https://user-images.githubusercontent.com/113462727/194705585-1507fcc3-70f9-4d44-adb6-b6136e3fc318.png)

Flag2 (or the 3rd flag) hint says that you should inspect Element on the form when creating a new post. So again click **Write a new post**, right click on the page and choose inspect element. What pops out should be the **input type="hidden"**. That text is saying there is a user_id who's value is 3 for me is hidden. If I change that hidden to text, the page will show the value.


![image](https://user-images.githubusercontent.com/113462727/194705854-e69b49c8-77ad-4099-a6d0-66627436f9cf.png)

If we create a new post and change that value, we're essentially changing the user value to another and creating a post as a different user.

![image](https://user-images.githubusercontent.com/113462727/194705945-710803a1-cc37-439c-aa39-75c68fd8d792.png)

You can see at the bottom the account has changed from **iamauser** to **user**


![image](https://user-images.githubusercontent.com/113462727/194705993-099e3673-1958-4186-9ef6-2d236c01c3d5.png)








