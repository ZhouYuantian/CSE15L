Thid bolg is going to guild you how to access UCSD server via terminal in VSCODE.
First thing is to install VSCODE:https://code.visualstudio.com/
After you install, open it and you should see a page like this:
![image](https://user-images.githubusercontent.com/46364362/149471159-d59ad599-57b9-4963-8aab-ab5d46ccb578.png)
clike the "terminal" on the tool bar and then you can access the terminal like this:
![image](https://user-images.githubusercontent.com/46364362/149471279-3dea224c-896c-48c9-88e3-2c4e8b4147c3.png)
then, you can input the command line code in the terminal.
Now, you may need to install openSSH for remote connecting: https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse
After openSSH setup, you can try the command:
![image](https://user-images.githubusercontent.com/46364362/149472737-dff43ddf-8d76-4b83-9b23-50f16388e907.png)
where zz should replace by your course specfic account.
type in your password and you will recieve a message aking you confirm, type "yes" and press Enter.
![image](https://user-images.githubusercontent.com/46364362/149473631-08610ae9-bf3e-4fde-94d5-60c4dac232d1.png)
This pitcrue indicate you have successfully login to the server.
you can try some command right now: ls, cd, ls-a. If you want to log out, type in "exit" or press Ctrl-D
Next you can try to move file to the sever from your computer:
Using 'cd' or 'cd' goes into the directory of the file that you want to move.
![image](https://user-images.githubusercontent.com/46364362/149475957-358436b6-c773-4f88-8394-05fc9ba4357b.png)
Using scp to move file to server like the pitcure did, scp fllows by the file name fllows by the account.
After that, login to the server and run 'ls', you should see the file you just moved in.
If you feel boring about inputing the password every time when you login, you can setup a SSH keys:
![image](https://user-images.githubusercontent.com/46364362/149482006-b624ac89-80ba-4365-988c-46323ca47560.png)
enter the file directory fllows by the code above. And then it will ask you entering passprhase.
clik enter if you don't need.
Then it will show you your key fingerprint and the key's randomeart image.
If you are in Windows, you may need to run these few linesin PowerShell in order to make the key works:
'Get-Service ssh-agent | Set-Service -StartupType Manual'
![image](https://user-images.githubusercontent.com/46364362/149487559-47f1829c-cf19-4368-93b5-54e932551e8e.png)
next:
you need to copy the punlic key to the .ssh directory which is the .pub file that just been create.
![image](https://user-images.githubusercontent.com/46364362/149489194-08c1235f-e943-4d68-938b-7e8bcc39d2bb.png)
using the path you saw above.
Futheremore, if you want some more convinience, you can run file or commands in your computer without login to server.
![image](https://user-images.githubusercontent.com/46364362/149489882-beae9816-06f7-4cf0-8c5b-29d918461373.png)
quote the commands you want to run at the end of the ssh sentence. this will let you run the command in the server but without login.
