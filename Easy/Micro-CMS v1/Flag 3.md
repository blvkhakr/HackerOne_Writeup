This would also be considered Flag2 on HackerOne, but we're counting regular here and not with an index starting at 0.
Again we start here at the home page

![image](https://user-images.githubusercontent.com/113462727/194417484-a58851e0-5c66-459b-9c27-58de7c9a1309.png)


Hints: sometimes a given input will affect more than one page & the bug you're looking for doesn't exist in the most obvi place this input is shown.

You'll need to create a page and throw a script in the body of the page. Don't forget to add quotes in the alert, forgot to do that here and needed to.

![image](https://user-images.githubusercontent.com/113462727/194420611-0963b4b7-3b0f-44b8-b970-e1456cb7ed82.png)

Once you back back to the page, you'll see the flag pops up in a JavaScript alert. A classic cross site scripting vulnerability.

![image](https://user-images.githubusercontent.com/113462727/194420930-1843b0a7-5d56-46c5-b19f-c76c8989d5ca.png)

