Lightweight, fully-featured timer program written entirely in bash

## Features
- Both countup and countdown timers
- Recurring timer function
- Smart time parsing
- Persistent across reboots (and even computers if .timer file is synced)
- Low resource usage (files are changed only on commands and timer expiry)
- Very few dependencies
- Multiple alarm functions (sound, custom script, and more)
- Single undo

## Demo
(Demo goes here)

## Getting started
### Dependencies
- [entr](http://entrproject.org/)
- sed
*Optional*
- libnotify (to get notifications when timer expires)

### Installation
```
git clone git@github.com:vividn/timer.git
cd timer
sudo ln -s $PWD/timer /usr/local/bin/timer
```

## Commands
Timers are issued commands with the following syntax
`timer [*n*] *command* *args*`, where `*n*` is the timer number. If `*n*` is omitted timer 1 is assumed.

| Command | Action | Args |
|---------|--------|------|
| `set`,`s` | Sets and starts a countdown timer | Duration |
| `pause`,`stop` | Pauses a currently running timer | |
| `start`,`go`,`play` | Resumes a paused timer, or starts a countup timer |  |
| `toggle`,`p`,`pp` | Toggles pause state of timer |  |
| `zero`, `z` | Resets the timer to +00:00 |  |
| `recur`, `r` | Sets and starts a recurring countdown timer | Duration |
| `from`, `until`, `til`, `to` | starts a timer relative to the time specified | Time |
| `plus`, `+`, `add` | Adds *Duration* to the timer | Duration |
| `minus`, `-`, `sub` | Subtract *Duration* from the timer | Duration |
