# watchrun

A simple bash event loop for triggering anything after saves.

Just give it a path to watch followed by a hyphen, followed by a hyphen-delimited list of commands to run. It'll run them sequentially, and then set up to detect new changes in the path. Loops until you kill it.

## Examples!

Make your source code with every tweak!
```
$ watchrun . - make
```

Build and rsync your grunt project with each save!
```
$ watchrun . - grunt build - rsync -ravP ./ gmarchin@some.server.com:./
```

Keep TPS reports from falling through the cracks! (Requires https://github.com/EvanHahn/pushbullet-cli)
```
$ watchrun ~/Documents - pb -a "Quit putting stuff in Documents! You're just gonna forget about it!!"
```

Have a REALLY granular git history with detailed commit messages! (PROBABLY DON'T ACTUALLY DO THIS! YOUR COWORKERS ARE HASSLED ENOUGH!)

```
$ watchrun . - git add --all - git commit -m "Some fixes." - git push --all
```
