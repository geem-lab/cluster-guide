## Basic usage 

Ask for Prof. Giovanni for a user, if one is granted you can login to the cluster using IP:150.162.31.2 and Port:2222 as follows.

```console
$ ssh your_user@150.162.31.2 -p 2222
``` 
When logging in the cluster for the first time, please update your password to a [strong](https://edu.gcfglobal.org/en/internetsafety/creating-strong-passwords/1/) one.

If you don't want to remember the port and the ip everytime you login, you can [register](https://linuxize.com/post/using-the-ssh-config-file/) this remote location in your ~/.ssh/config file (you can change jupiter for any name of your choice).

```
Host jupiter
    HostName 150.162.31.2
    User your_user
    Port 2222
``` 

Now you can login with:

```console 
$ ssh jupiter
```

You can also set a passwordless connection by [creating a key and making it available in **jupiter**](https://phoenixnap.com/kb/setup-passwordless-ssh).
