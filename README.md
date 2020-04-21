# Quick and easy git

Git is probably one of the top tools I use for code management and something I probably should have adated sononer than later. This guide is more of a reference for myself of everything I've learned so I don't have to google or search stackoverflow as much. If you think of something else to add to this, please feel free to contact me. 

### Cloning a repositiory and adding an SSH key 
To start working with a project, either one you've created or someone else had created, we can clone the repository and link it to a ssh key so we can interactively edit it and quickly push updated back to github.

To get started, we need to first generate a public ssh key to provide to github. This is a way to authenticate us to edit something within your own github account so we don't have to sign in each time we want to make a change. Trust me, this is worth it.

Open either Terminal (MacOS), Ubuntu (Linux/Windows), or Git Bash to open up a shell terminal. 
To generate a public key, we can type the following command:
```bash
ssh-keygen -t rsa -b 4096 -c "your_email.domain.com"
```

This provides us with various instruction about where to save the key and if we want to add a passphrase. 
```bash 
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/username/.ssh/id_rsa):
```
Here is will hit enter so it saves in the default location. It will then ask us to save a passphrase. I personally just hit enter twice, but it up you if you want a passphrase for protection.

```bash
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

Our key will be proberly generate when you get an output that looks similar to this:
```bash 
Your identification has been saved in /Users/username/.ssh/id_rsa.
Your public key has been saved in /Users/username/.ssh/id_rsa.pub.
The key fingerprint is:
01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db your@email.com
The key's randomart image is:
+--[ RSA 2048]----+
|                 |
|                 |
|        . E +    |
|       . o = .   |
|      . S =   o  |
|       o.O . o   |
|       o .+ .    |
|      . o+..     |
|       .+=o      |
+-----------------+
```

We then want to obtain the public key and add it to our github profile. To display the sequence, we can use the following command.
```bash
$ cat ~/.ssh/id_rsa.pub
```
We can then copy this output and pull up our github page. 



