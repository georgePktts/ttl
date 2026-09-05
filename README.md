ttl (time to leave)
---
A tiny CLI that counts down to when your shift expires.

## What it does
`ttl` tells you how much time is left until you leave work. Set your leave time once, and every time you run it, it shows you the countdown.

```bash
ttl
02:15

ttl --long
You have 02h 15m
```

Once your leave time has passed, it shows a custom message instead:

```bash
ttl
Go go go!
```

## Install
Download the script, make it executable, and drop it somewhere in your `PATH`:

```bash
curl -o /usr/local/bin/ttl https://raw.githubusercontent.com/georgePktts/ttl/main/ttl
chmod +x /usr/local/bin/ttl
```

Requires `bash`. Works on Linux and macOS.  
Tested on macOS.

## Usage

```txt
usage: ttl [--time time] [--message message]
ttl calculates time to leave

options:
  -h, --help              display this help and exit
  -l, --long              display full time
  -m, --message message   set leave message. Default Go go go!
  -t, --time time         set leave hour in HH:MM format
      --version           display version info and exit
```

On first run (or whenever no leave time is set), `ttl` will ask you for it interactively. From then on, your settings are saved and reused automatically:

```bash
ttl -t 17:00
```

You can update your leave time or message at any point the same way:

```bash
ttl -t 18:00 -m "Beer time!"
```

## Configuration
Settings are stored in `~/.config/ttl/ttl.conf`.

## Why
Because I wanted a fun weekend project, and Time To Leave was a name I couldn't pass up.

## Licence
MIT - see [LICENCE](LICENCE) for details.
