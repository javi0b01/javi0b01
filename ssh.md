# :memo: Notes
## SSH
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [OpenSSH](https://www.openssh.com/manual.html)
- [GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
- [GitLab with SSH](https://docs.gitlab.com/ee/ssh/)
- [Bitbucket with SSH](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/)
- [PuTTY](https://www.putty.org/)
### Terms and concepts
- SSH
- SSH server
- SSH client
- Private key
- Public key
#### Basic commands
Install
```
$ apt-get install openssh-server
$ systemctl status ssh
$ systemctl enable ssh
```
Key
```
$ ssh-keygen
$ eval $(ssh-agent)
$ ssh-add
$ ssh-add -D
```
Tests
```
$ ssh -T git@github.com
$ ssh -T git@gitlab.com
$ ssh -T git@bitbucket.org
```
Connect
```
$ ssh <user>@<ip>
$ .ssh/authorized_keys
```
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
