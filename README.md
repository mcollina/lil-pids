# lil-pids

Dead simple process manager with few features

```
npm install -g lil-pids
```

First create a file with the commands you wanna have running

```
# assuming this file is called 'services'
node server.js
node another-server.js
```

Then simply start lil-pids with the filename

```
lil-pids ./services
```

It'll watch the file so every time you update it, old processes
no longer referenced from the file will be shutdown and any new ones will be spawned.

lil-pids will forward all stdout, stderr to its own stdout, stderr prefixed with the process id.

It will also tell you when a command has been spawned, exited and finally it will restart processes
when the crash/end.

That's it!

## Pro-tip

Spawn lil-pids /home/username/services with your OS' service monitor. Then it'll startup at boot
and every thing you'll need to do is edit the services file

## License

MIT
