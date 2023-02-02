# SSH-Tips

## Disable root

Adding a user to the sudoers group allows that user to execute commands with superuser (root) privileges by prefixing a command with sudo. This allows for fine-grained control over which users can perform which actions with superuser privileges.

Having the root account share the same password as a regular account, on the other hand, means that any user with access to the password can directly log in as the root user. This is less secure and not recommended, as it provides less visibility and control over who is using the superuser privileges and what actions are being performed.

Also, if an attack is set to target `root@ip`, by disabling root access it's impossible to create a connection through the root user.

In summary, using sudo provides better security and accountability by allowing only specific users to execute specific commands with superuser privileges, while sharing the root password with a regular user account provides no such controls.

Inside the server, create a new user with sudo access:

```bash
adduser {"USER_NAME"}
usermod -aG sudo {"USER_NAME"}
```
## Add SSH Key  

Generate ssh-key from local device:

```bash
ssh-keygen {Extra flags}
```

The .pub key generated can be used to access the server without the created user password. It has to be copied to the server:

```bash
cat {"GENERATED_KEY"}.pub | ssh {"USER_NAME"}@{ip} "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys"
```

alternative:

```bash
ssh-copy-id -i {"PATH_GENERATED_KEY/GENERATED_KEY.pub"} {"USER_NAME"}@{ip}
```
The key without the `.pub` extension MUST NOT BE SHARED.

## Change Port and Config

SSH uses port 22, a better way to avoid port scanning or some sort of attack performed by bots analyzing random ip addresses that eventually compromises one of our servers could be changing the port.

The config file can be accessed following the steps:

```bash
sudo nano /etc/ssh/sshd_config
```

Usual Changes:
> Port (not 22)
> 
> PermitRootLogin no
> 
> PasswordAuthentication no

Now, only clients with an allowed ssh-key have access and root user is disabled when establishing the ssh connection.

After applying the changes, restart the service; using systemctl:

```bash
sudo systemctl restart sshd
```
> NOTE
> 
> On the client, the port must be specified, with a flag as following `ssh {"USER_NAME"}@{ip} -p {PORT}`


## Other Tools

Uncomplicated Firewall, really useful to block ports and disable ping responses.

With ufw, firewall rules can be set using a set of predefined commands and profiles, allowing the user to quickly configure the firewall to block or allow specific types of incoming and outgoing traffic. 