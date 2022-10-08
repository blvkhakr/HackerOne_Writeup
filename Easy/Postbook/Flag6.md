Last flag here and the hint -- Deleting a post seems to take an ID that is not a number. Can you figure out what it is?

Best way to do this is create a post to delete. Once the post is created, right click and go to inspect of that page.

![image](https://user-images.githubusercontent.com/113462727/194707767-9fce0b3d-24ab-43a6-85df-33015a6be36b.png)


Drop down to the div that contains a reference to the actual post.


![image](https://user-images.githubusercontent.com/113462727/194707808-30f8b00c-d499-487b-a421-360c5ed19c00.png)


There's a hash there that's similar to what we found for the user cookie. You get the hash and unhash it by MD5 and find that the number is 9 (for me).
The number is associated with the page or post number. Meaning if you change that post number to be on that was already created like say...2, we can delete it.

![image](https://user-images.githubusercontent.com/113462727/194707870-7a997c45-111d-4895-8cfd-845a682db647.png)

Get the MD5 hash of page 2 or of just another post already there, replace the original hash for the newly created one and click delete on the newest post you
you created.

![image](https://user-images.githubusercontent.com/113462727/194707999-79bf7814-c5ef-4c20-8393-e74f009e7a46.png)


you'll see that your original post is still there and you'll receive the last flag.

![image](https://user-images.githubusercontent.com/113462727/194708092-1e75baac-331b-4f27-b8f8-1a6691136574.png)
