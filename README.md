## Add Automator to run appleScript

- open `Automator`, select `Service`
- search for `applescript` and select `Run AppleScript`
- select from `Service receives` -> `no input`
- add `do shell script` as in this example and save it

```
on run {input, parameters}
  do shell script "usr/bin/osascript ~/Documents/appleScripts/inspect_ios.scpt"
  return input
end run
```

## Add shortcut for Automator
- open `System Preferences` -> `Keyboard` -> `Shortcuts`
- select `Services` -> `General` -> `your_script_name`
- desired shortcut

### Read more here
- [Apple post](http://apple.stackexchange.com/questions/100642/how-to-make-an-existing-applescript-file-to-work-as-a-service)
