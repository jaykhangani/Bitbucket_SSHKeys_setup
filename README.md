#Setting Up Bitbucket's SSH Key for Beginners
##Step 1:Ensuring U have a SSH Client
1. Open a Terminal and write : ```ssh -v``` and press Enter
2. if something like below comes then you have ssh installed :  

```usage: ssh [-1246AaCfgKkMNnqsTtVvXxYy] [-b bind_address] [-c cipher_spec]  
           [-D [bind_address:]port] [-e escape_char] [-F configfile]  
           [-I pkcs11] [-i identity_file]  
           [-L [bind_address:]port:host:hostport]  
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]  
           [-R [bind_address:]port:host:hostport] [-S ctl_path]  
           [-W host:port] [-w local_tun[:remote_tun]]  
           [user@]hostname [command]```  

----------------
##Step 2:Setting up Default Identity
1. Open up a Terminal and write : ```ssh-keygen``` and press Enter
2. It will ask you for a file name ,it should be kept empty and you should press Enter
3. It will ask you for some phrase,you can write it or keep it blank but you should remember it 
4. It will create a Fingerprint and RSA image and will show you something like this  

```myhost:~ manthony$ ssh-keygen    
Generating public/private rsa key pair.  
Enter file in which to save the key (/Users/manthony/.ssh/id_rsa):   
Created directory '/Users/manthony/.ssh'.  
Enter passphrase (empty for no passphrase):   
Enter same passphrase again:   
Your identification has been saved in /Users/manthony/.ssh/id_rsa.  
Your public key has been saved in /Users/manthony/.ssh/id_rsa.pub.  
The key fingerprint is:  
4c:80:61:2c:00:3f:9d:dc:08:41:2e:c0:cf:b9:17:69 manthony@myhost.local  
The key's randomart image is:  
+--[ RSA 2048]----+  
|*o+ooo.          |  
|.+.=o+ .         | 
|. *.* o .        | 
| . = E o         |  
|    o . S        |  
|   . .           |  
|    .            |  
|                 |  
|                 |  
+----------------```  
5. This will also create a hidden directory in home folder with name :``` .ssh```    

##Step 3 :Install the key on your Bitbucket Account 
1. Open a Terminal and write :``` cat ~/.ssh/id_rsa.pub```
2. It show the RSA key , copy it .
3. Now go to you Bitbucket Account.
4. Click on the profile icon on right corner of Bitbucket.
5. Click on Manage Account Tab.
6. Go to  on SSH Keys in Security Tab.
7. Click on Add Key.
8. Write a unique name for label of key eg. Linux-PC-Model-name-date
9. Paste the RSA key earlier copied.
10.Click save and You are Done!!!!

Wasn't it Damn easy??!!  

If you have an issues them please report it on the issue tracker.  
[https://github.com/jaykhangani/Bitbucket_SSHKeys_setup/issues](https://github.com/jaykhangani/Bitbucket_SSHKeys_setup/issue)	


