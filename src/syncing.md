## Transfering files 

The most common way of transferring files between local and remote locations (and the easiest if you're just starting) is the [scp](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/) command. 

For istance, if you want to send a `opt.inp` file located at `~/geem/projects` to a `/home/your_user/projects/` folder located in jupiter:

```console 
$ scp ~/geem/projects/opt.inp jupiter:/home/your_user/projects/ 
```

Or the other way around, from jupiter to your local folder:

```console 
$ scp jupiter:/home/your_user/projects/opt.out ~/geem/projects/
```

There are other options (for instance, [rclone](https://rclone.org/commands/rclone_sync/)) that can be also be used to sync files between your local machine and jupiter. 

If you're using a windows machine, a good graphical interface that allows you to drag and drop files is [mobaxterm](https://mobaxterm.mobatek.net/).

[Vinicius](https://github.com/caprilesport) also has a [script](https://github.com/caprilesport/scripts/blob/master/csync) that syncs and submits jobs while in your local machine, any doubts talk to him. 


