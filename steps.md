# SSH Setup

1. Generate a key `ssh-keygen -t ed25519 -f ~/.ssh/<name_of_key> -C <email>`
2. Copy key to server: `ssh-copy-id -i ~/.ssh/<name_of_key> username@ip_of_server`
3. Update SSH config file:
 ```
 Host media-test
  HostName <ip_of_server>
  User username
  IdentityFile ~/.ssh/<name_of_key> 
  IdentitiesOnly yes
 ```