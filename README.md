# Quick and easy git

Git is probably one of the top tools I use for code management and something I probably should have adated sononer than later. This guide is more of a reference for myself of everything I've learned so I don't have to google or search stackoverflow as much. If you think of something else to add to this, please feel free to contact me. 

### Cloning a repositiory and adding an SSH key 
To start working with a project, either one you've created or someone else had created, we can clone the repository and link it to a ssh key so we can interactively edit it and quickly push updated back to github.

To get started, we need to first generate a public ssh key to provide to github. This is a way to authenticate us to edit something within your own github account so we don't have to sign in each time we want to make a change. Trust me, this is worth it.

Open either Terminal (MacOS), Ubuntu (Linux/Windows), or Git Bash to open up a shell terminal. 
To generate a public key, we can type the following command:
```bash
ssh-keygen -t rsa -b 4096 
```

This provides us with various instruction
