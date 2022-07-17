# vscode-backup
**Fonts**
 - Operator Mono Medium
 - Fira Code

### Backup
1. Make backup directory  
`mkdir /home/$USER/code-backup && cd /home/$USER/code-backup`
2. Backup Extensions  
`code --list-extensions | xargs -L 1 echo code --install-extension > ext`
3. Backup Settings  
`cd /home/$USER/.config/Code/User`  
`tar -czf code-config.tar.gz *.json`  
`mv code-config.tar.gz /home/$USER/code-backup`

### Restore
*Go to backup directory first on terminal*

1. Install Extensions  
`chmod +x ext`  
`./ext`
2. Restore Settings  
`tar xzf code-config.tar.gz`  
`mv *.json /home/$USER/.config/Code/User`

Source : [https://blog.dzarsky.eu/how-to-backup-your-vs-code-extensions-and-settings](https://blog.dzarsky.eu/how-to-backup-your-vs-code-extensions-and-settings)
