To run a command on bg:
```
command &
```
This will show the process id in square brackets.  

To bring a foreground process to background, press CTRL + Z. This will suspend the process.
Enter `bg` command to resume the process in background.

To show all running/stopped bg processes:
```
jobs -l
```

To kill the process:
```
pkill PID
```

To bring to foreground:
```
fg %PID
```