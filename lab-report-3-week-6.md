

# 1. Streamlining ssh Configuration
## My .ssh/config file:

![image](https://user-images.githubusercontent.com/46364362/167041966-2f4d7e87-4c80-4f7e-adb2-b2e1bad0633f.png)

## logging into my account using just the alias:
This help us login without enter username which is very convinient.

![image](https://user-images.githubusercontent.com/46364362/167042030-97b757e5-778e-41d5-a959-e802e9561216.png)

 ## Using scp command copying a file to my account using just the alias:
 

![image](https://user-images.githubusercontent.com/46364362/167042471-264b3aad-2043-455a-8a4f-b3120a1e80b5.png)

# 2. Setup Github Access from ieng6
This enable us to commit&push changes to github from server.

## Public&private key I made stored on Github and in my user account:

![image](https://user-images.githubusercontent.com/46364362/167068268-79fbd37f-4ea1-4ae8-9ecb-6ce236b689a1.png)

![image](https://user-images.githubusercontent.com/46364362/167066778-83d10b51-5a0f-49ca-b978-71af2c5aca04.png)

# 3. Copy whole directories with scp -r
This enable us to copy a full directory at once instead repeatly copy the files manually.

##  Copying whole markdown-parse directory to ieng6 account:
basicly we just need to enter to the directory and then we can use scp -r command to copy recursively.

![image](https://user-images.githubusercontent.com/46364362/167072294-be3730c2-4272-46d6-a8b0-cb5280da9aca.png)

## Login and complie after copy:
we can run the test right now that we just copy:

![image](https://user-images.githubusercontent.com/46364362/168420069-22001dfc-7487-4151-8fdb-1f850d62b618.png)


## Combining scp, ;, and ssh and complie all in one line:
This make it even more convinent, we can finish all the thing in one line and without login to the server.

![image](https://user-images.githubusercontent.com/46364362/168420086-f609e8bb-1a87-4c3d-86a9-4cb3aed29117.png)
