# quickstart
## Configure
Edit keys and processes in `quickstart`:
```sh
keyX="some byte"

procX() {
    # your custom process here
    pkill terminator
}
```
Add process entry to switch-case:
```sh
...
    case $byte in:
        ...
        $keyX)
            procX &
            ./terminator $!
            ;;
        ...
```

Example:
```sh
key1="a"

proc1() {
    echo "a"
    pkill terminator
}

...
    case $byte in:
        ...
        $key1)
            proc1 &
            ./terminator $!
            ;;
        ...
```

## Run
```sh
./quickstart
```
Any of the smaller four buttons can be used to start a process. When starting `quickstart` through integrated terminal or ssh, any character available on the keyboard can be used.
When the middle button is pressed (this corresponds to a `\n` character and is handled by `terminator`), the process gets killed.
