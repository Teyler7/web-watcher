## Install on a Server

Run:

```shell
$ go build -o web-watcher .
``` 
to compile the program via GO.

The set a command that runs on start up with `sudo nano /etc/rc.local`. Set the path:

```shell
$ [[pwd path to ./web-watcher]] --interval 1 --token XXXXXXXXX 2>> output.log &
```

This will create an output.log file in the directory that will be gitignored. You can checkout the constant output with `tail -f output.txt`