Heads up!!! The method I'm going to use here is actually a huge cheat to this challenge. It would be best to use a combination of UNION attacks for Flag0, a call using curl for Flag1 and sqlmap for Flag2. I used SQLmap and got way mroe than I bargained for so if you want to see that method, keep reading on.


So we're back on the CMS page and see that they've made some changes. Again we're anti on the Index starting at 0 and chose to do 1 instead. Meaning on HackerOne this Flag is actually Flag0 and not 1.

![image](https://user-images.githubusercontent.com/113462727/194677573-ab4a4687-c872-4ccc-bb75-4a06e2e151e8.png)

After clicking on Micro-CMS Changelog

![image](https://user-images.githubusercontent.com/113462727/194678429-bc0bfd4a-588b-48ff-8a02-26e85bb7da69.png)

If you try to edit any pages or increment the pages you'll only be met with a login page. So now we have to actually bypass the login. How do we do that? By using a handy tool called SQLmap. There are other ways to do this like UNION attacks, which are a bit more manual. I don't mind using those but in this case I wanted to be more proficient at automation so I used a tool. 

You can install SQLmap by following the directions listed [here](https://sqlmap.org/). For this flag, I used a combination of Burp x SQLMap. I captured the request with burp and threw the text version of that request in sql map. See the below screenshots.


Go to the login page (from either edit page or tampering w/ url, whichever) and capture a request via the Burp Proxy. Type whatever you want for user/password. It doesn't matter because you don't actually have the creds, but you do need this for the next step.

![image](https://user-images.githubusercontent.com/113462727/194682523-2c49c61a-a3ed-470e-886b-e4af6bce650a.png)


Right click on the request and save it as a file on your computer. Now run the following sqlmap command: **sqlmap -r <request_txt_file> --dbs**

NOTE: your command may look a little different from mine but it's some variation of the above command. Run the program, -r for request using the file and then look at the databases. Also, to save time, just say no to all the questions they ask. It isn't necessary for this level.


![image](https://user-images.githubusercontent.com/113462727/194682606-643f6825-749d-4129-997d-3175ed1596fe.png)


You should see the tables now. You can search all of them but the only table that actually matters is **level2**
![image](https://user-images.githubusercontent.com/113462727/194683010-9bdb4edb-6101-4e4c-8ae9-7626b1e4b40d.png)


Now you want to look at the tables in Level2 so run the following command: **sqlmap -r <request_txt_file> -D level2 --tables**

Viola! Tables

![image](https://user-images.githubusercontent.com/113462727/194682960-e1f5d519-288c-478d-96e5-031959ec72b2.png)


So the next thing I want I want to do is dump those tables. Admin must be holding all the credentials and pages must be holding all the pages, meaning the hidden page is in there as well (if you've been searching around you would've seen this.) So to dump the tables (there's a more elegant way of doing this if an application has more than one table, but knowing there aren't that many tables or that much information for this application I used the following command to dump both tables:  **sqlmap -r <request_txt_file> -D level2 --tables -dump**


We're able to see the hidden page 3 and there's a flag. Looks like we also have the user/password for the admin login as well


![image](https://user-images.githubusercontent.com/113462727/194683808-adc2bbeb-0e0e-4fc8-a5e1-46376aa76213.png)

