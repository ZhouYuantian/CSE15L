## CSE 15L Lab Report 1

Thid bolg is going to guild you how to access UCSD server via terminal in VSCODE.
## Install VSCODE
First thing is to install [VSCODE](https://code.visualstudio.com/)

![image](https://user-images.githubusercontent.com/46364362/163670057-cb43cd9c-d660-42c7-9e3a-fa63c6ec4b87.png)


Clik that blue buttom to download.

After you install, open it and you should see a page like this:
![image](https://user-images.githubusercontent.com/46364362/149471159-d59ad599-57b9-4963-8aab-ab5d46ccb578.png)
clike the "terminal" on the tool bar and then you can access the terminal like this:
![image](https://user-images.githubusercontent.com/46364362/149471279-3dea224c-896c-48c9-88e3-2c4e8b4147c3.png)
then, you can input the command line code in the terminal.

## Remotly Connecting
Now, you may need to install [openSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) for remote connecting: 
After openSSH setup, you can try the command:
```
# $ssh cs15lsp22zz@ieng6.ucsd.edu
```

where zz should replace by your course specfic account.
type in your password and you will recieve a message aking you confirm, type "yes" and press Enter.

![image](https://user-images.githubusercontent.com/46364362/149473631-08610ae9-bf3e-4fde-94d5-60c4dac232d1.png)

This pitcrue indicate you have successfully login to the server.

## Try Some Commands
you can try some command right now: ls, cd, ls-a. If you want to log out, type in "exit" or press Ctrl-D

## Moving File with SCP
Next you can try to move file to the sever from your computer:
Using 'cd' or 'cd' goes into the directory of the file that you want to move.

```
# $scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/
```

Using scp to move file to server like the pitcure did, scp fllows by the file name fllows by the account.
After that, login to the server and run 'ls', you should see the file you just moved in.

## Setting an SSH Key
If you feel boring about inputing the password every time when you login, you can setup a SSH keys:

```
#
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
```

enter the file directory fllows by the code above. And then it will ask you entering passprhase.
clik enter if you don't need.
Then it will show you your key fingerprint and the key's randomeart image.
If you are in Windows, you may need to run these few linesin PowerShell in order to make the key works:

```
'Get-Service ssh-agent | Set-Service -StartupType Manual'
```

![image](https://user-images.githubusercontent.com/46364362/163669642-b6c10fa9-ebc8-47a6-88a2-384ddb57124a.png)

After it finish, it should display like the following image:

![image](https://user-images.githubusercontent.com/46364362/163670209-d25fe1b5-4592-4110-843e-f476f9a86baf.png)



next:
you need to copy the punlic key to the .ssh directory which is the .pub file that just been create.

```
$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
```

using the path you saw above.

## Optimizing Remote Running

Futheremore, if you want some more convinience, you can run file or commands in your computer without login to server.

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"
```

quote the commands you want to run at the end of the ssh sentence. this will let you run the command in the server but without login.
It save a lot of keystrokes since you don't need to type in your password right now, and you don't need to exit after that command ran.
