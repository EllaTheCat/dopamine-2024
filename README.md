# dopamine-2024 README.md
## Status 08 November 2023

This repository exists because my top priority is to get an offsite backup of my sway environment, and
hence that's all it is for the moment, a backup. I want to share my documented configuration soon, so I
might as well let my alter-ego Ella the Cat put her marketing hat on to keep you interested.

## What's in it for me, the developer?

I was diagnosed with **Parkinson's Disease **(PD) back in 2014. I like messing with computers. I don't want
PD to stop me programming. I don't want people to think PD has made me stupid.

The project is a working configuration for **Sway, a tiling window manager**. It is the capabilities of Sway
that make it accessible. Sway automates window placement  so I need not, but more to the point, when PD
tremor kicks in, I simply can't manipulate windows without sway or i3. I need my meds and a keyboard and
automation. Autotiling is a third party program that decides which way to split Sway or i3 windows. I
have direct access to 100 workspaces, and these can be scripted to show various apps or documents.

## What's in it for you?

Take whatever you want, but please give me attribution for my work and attribute others for
theirs. Abide by the license is all you must do but be kind and considerate pkease. If this project
helps you or someone you know in any way with accessibility or Parkinson's my imposter syndrome would
like to know.

## Features

- **Modifier-centric and mode-centric bindings on the same keys** so you use what works for you. For
    example my left hand uses modifiers, my right hand needs modes.

- **100 workspaces with customisable and or scripted behaviours.** Example bash scripts for editor and
    browser workspaces.

- **Four status bars with dual monitor systems.** Yes you can show or hide them altogether or
  individually. The two lower edge status bars are reserved for binding mode indicator and workspace
  tags. The upper edge status bars include an ascii-art animated thermometer for monitoring CPUs, disk
  usage and temperatures, status of helper programs, a clock.

- **3 tables of 100 user definable commands filled with examples ** : setting window opacity, scaling
  workspaces for when you're tired, a few TV channels, sway manpages, i3 user's guide, combi workspaces
  of app and browser, utilities such as getting app_id, shellcheck your scripts, put your phone in a
  sway container, make a sway window bigger than  one screen for snazzy wallpaper, widescreen movies,3
  "total emacs immersion" or just doing your makeup.

- **Startup.** A example copy of my startup config file to get things moving in the morning.
Tunes. Email. Browsers with your preferred pages or folders preloaded. Emacs server and client per
instance workspaces.

- ** Shutdown**. A really simple and fast way to get away from the computer without subsequent worry
that you've forgotten to do something.

- **Online help framework.** I use framework in the industry standard adjectival sense, to mean half-finished,
ready to explain the obvious and no help at all with the obscure. Here's what's coming:

- **Binding Mode Indicator**, a dark text on dazzling yellow background, that tells you that you're not in
Kansas anymore, but in a non-default mode where keys do different things compared with their usual
behaviour. Our correspondent Mr Jones the butcher reminds us DO NOT PANIC: First, if the UI freezes or
keys go dead then your typo has put you in a surprise mode by mistake and second, that if you are not
in default mode ** PRESS SPACE ** to get back there.

- The **green nagbar** that appears at the bottom edge of the screen at startup, whence it was called the
Welcome baanner, but has since evolved so it can be hadden or shown on demand (Super + Shift +
Escape|Caps). When visible, the green banner provides online help and request buttons operable by mouse.

- **Help topics,** prefixed "about" cover an intro, modes, keys, menus, workspaces. They are shell scripts
which load themselves as free form text to be displayed in Emacs, but could be Markdown or asciidoc as
determined by the script shebang, ooh..

- **[context sensitive help]** is one button but what you see depends on the mode (binding state), so
all modes can have relevant documentation displayed on demand,. Even if it is just the bindings code
reformatted, it's up to date.

- The sway **reload button**, sway **exit button** and nagbar **dismiss button** are mouse buttons, so
  you can't easily invoke them using the keyboard.

## Immediate Tasks

I developed this for my own use so have not been as hard on myself as I would be professionally. These
are the things I have to do in the short term for this project to become shipshape.

- **BREAKING NEWS** I'm putting stuff on github regardless.

- **Comments in code** I was intending to put all documentation in the code as comments. I intend to
purge it in favour of the green nagbar help topics.

- **$HOME $USER**
Fix numerous hardcoded  "/home/ellathecat" strings, with sway config variables and bash variables.

- **ShellCheck Scripts**
Every script to pass ShellCheck by hand. Automation not a shipshape requirement.

- **One Config Review **
Concatenate all configs into one, strip comments and blank lines, insert file boundaries. Ask sway
reddit how to run the nagbar validation on it.

- **About Workspaces **
All the help topics to have something of substance written.

- **Context Help **
Not a shipshape requirement beyond an empty document with the correct title.