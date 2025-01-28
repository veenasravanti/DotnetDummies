# DotnetDummies updated
1. Open Git Bash:
    Use Git Bash for managing SSH keys.
    Check for Existing SSH Keys:
    ls -al ~/.ssh

    Lists files in the .ssh directory to check for existing keys.
2. Generate a New SSH Key (if needed):
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    Generates a new SSH key pair.
3. Add Your SSH Key to the SSH Agent:
    eval "$(ssh-agent -s)"
    ssh-add ~/.ssh/id_rsa

    Starts the SSH agent and adds your private key.
Add Your SSH Key to Your GitHub Account:
cat ~/.ssh/id_rsa.pub

Copies the public key to your clipboard.
Go to GitHub Settings > SSH and GPG keys > New SSH key and paste your key.
Configure SSH in Visual Studio:
Open Visual Studio.
Go to Tools > Options > Source Control > Git Global Settings.
Ensure the SSH executable is set to “Git”.
Test Your SSH Connection:
ssh -T git@github.com

Tests your SSH connection to GitHub.