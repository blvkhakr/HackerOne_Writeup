The page you see at start up

![image](https://user-images.githubusercontent.com/113462727/189977581-03b09b82-1247-44e8-904e-011092359642.png)

After playing with the features you realize you can create a page. So I created a test page to start to playing around the features.

![image](https://user-images.githubusercontent.com/113462727/189977758-8c6cf746-88a3-4f83-8fb5-ae4cfb8228e1.png)

Once the page is created, you go back to the first page and see it's been added to the directory.

![image](https://user-images.githubusercontent.com/113462727/189979720-eeb2c69b-2cf6-4e1e-88f7-790a73507b7d.png)

When you click on the page you realize you can edit it. Hold this thought, it matters for the flag.

![image](https://user-images.githubusercontent.com/113462727/189977822-b12982a1-c749-4b9f-a692-4197b6dac609.png)

![image](https://user-images.githubusercontent.com/113462727/189978420-5a1548be-14bd-496e-908b-6a7dcdbdabb5.png)


Still playing around with the application, noticing that the page I created was number 9. So I started changing page numbers and found there was a forbidden page 4. You can't access it now...but remembering that there was the ability to edit the page...

![image](https://user-images.githubusercontent.com/113462727/189978590-9d8f57e3-f4f7-4302-a12f-0033cb7a37df.png)

Changed the URL to say page/edit/4 and viola! We're able to get the flag. **TIP:** This type of vulnerability is considered authentication/authorization bypass. I was able to accesss a forbidden resource without logging in because it wasn't properly locked down. I'm adding authorization bypass as well because it could've have been a priv user's resource.

![image](https://user-images.githubusercontent.com/113462727/189981476-d2e97cf4-c53c-48bd-831b-117f3cf914d9.png)
