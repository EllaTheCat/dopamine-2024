# dopamine-2024 README.md

This repository exists because my top priority is to get an offsite backup of my sway environment, and
hence that's all it is for the moment, a backup. I want to share my documented configuration soon, so I
might as well let my alter-ego [Ella the Cat](#about-us) put her marketing hat on to keep you interested.

## April Fool release

Another kitchen sink commit at start of March aimed at a release for April. I've been using the config
to see what works, broken it, fixed it, and this is now baseline.

- Less is more at startup. As I had hoped, I'm learning the workspaces, 33 for Emacs, the 5xy drop a
  terminal by workspace feels right, so the '999-$user.config' withers away.

- I have a shiny 3rd monitor, it's detachable, and sits underneath my two side-by-side monitors, so this
  config is still good for dual monitors only. I've kept the even-&-odd workspaces at left-&-right.
  I've kept to a side by side panorama for the backdrop.

- The super-fast reaper mode blew up in my face, it has been rewritten. Thanks bindsym --no-repeat.

 - Nautilus (45?) has started to play nice, even the indexing can be usefully applied, so it's default
   again.

- 60% compact keyboards have arrow keys by default, escaping / and ? is easier, and after much agonising
  Menu is on left side backslash by default for the foreseable future, right side is still possible.

## What's in it for me?

I was diagnosed with **Parkinson's Disease** (PD) back in 2014. I like messing with
computers. I don't want PD to stop me programming. I don't want people to think PD has made me stupid.

The project is a working configuration for **Sway, a tiling window manager**. It is the capabilities of
Sway that make it accessible. Sway automates window placement so I need not, but more to the point, when


Take whatever you want, but please give me attribution for my work and attribute others for
theirs. Abide by the LICENSE is all you must do but be kind and considerate please. If this project
helps you or someone you know in any way with accessibility or Parkinson's my imposter syndrome would
like to know.

## Features

- **Modifier-centric and mode-centric bindings on the same keys** so you use what works for you. For
    example my left hand uses modifiers, my right hand needs modes.

- **WASD keyboard** The main keyboard provides three inverted-T cursor keypads for focusing a container,
    moving a container, resizing a container. These can be mixed together, they can be used in default
    mode with the Mod4 modifier,or unmodified in a Menu mode entered by the Menu key. The Menu key
    provides two major modes, Menu Keys and More Menu Keys.

- **i3|sway keyboard** The WASD keyboard is more or less a simple rearrangement of the standard i3|sway
   layout we have all invested in. I intend to make the i3|sway standard bindings available as an
   alternative to WASD eventually. Note that with 100 instead of 10 workspaces (q.v.) the standard digit
   bindings have had to go.

- **100 workspaces with customisable and or scripted behaviours** Example bash scripts for editor and
    browser workspaces. To visit a workspace, press a dedicated key and then two digits, to move a
    container, press a different dedicated key and two digits. Three more dedicated keys provide three
    more tables.

- **3 tables of 100 user definable commands filled with examples:** setting window opacity, scaling
  workspaces for when you're tired, a few TV channels, sway manpages, i3 user's guide, combi workspaces
  of app and browser, utilities such as getting app_id, shellcheck your scripts, put your phone in a
  sway container, make a sway window bigger than  one screen for snazzy wallpaper, widescreen movies,
  "total emacs immersion" or just doing your makeup.

- **Four status bars with dual monitor systems.** Yes, you can show or hide them altogether or
  individually. The lower edge status bars are reserved for binding mode indicator and workspace
  tabs. The upper edge status bars include an ascii-art animated thermometer for monitoring CPUs, disk
  usage and temperatures, status of helper programs, a clock.

- **Startup.** A example copy of my startup configuration to get things moving in the morning.
Tunes. Email. Browsers with your preferred pages or folders preloaded. Emacs server and client per
instance workspaces.

- **Shutdown.**   A really simple and fast way to get away from the computer without subsequent worry
that you've forgotten to do something.

- **Online help framework.** I use framework in the industry standard adjectival sense, to mean half-finished,
ready to explain the obvious and no help at all with the obscure. Here's what's coming:

- **Binding Mode Indicator**, a dark text on dazzling yellow background, that tells you that you're not in
Kansas anymore, but in a non-default mode where keys do different things compared with their usual
behaviour. Our correspondent Mr Jones the butcher reminds us  **DO NOT PANIC**. First, if the UI freezes or
keys go dead then your typo has put you in a surprise mode by mistake and second, that if you are not
in default mode **PRESS SPACE** to get back there.

- A **green nagbar** that appears at the bottom edge of the screen can be hidden or shown on demand with
the binding Mod4+Shift+Caps. When visible, the green banner provides online help buttons operable by
mouse, also reload and dismiss buttons as on the red nagbar, and finally an exit button.

- **Help topics,** prefixed "about" cover an intro, modes, keys, menus, workspaces. They are shell scripts
which load themselves as free form text to be displayed in Emacs, but could be Markdown or asciidoc as
determined by the script shebang.

- **context sensitive help** is one button but what you see depends on the mode (binding state), so
all modes can have relevant documentation displayed on demand,. Even if it is just the bindings code
reformatted, it's up to date.

## Immediate Tasks

I developed this for my own use so have not been as hard on myself as I would be professionally. These
are the things I have to do in the short term for this project to become shipshape.

- **Comments in code** I was intending to put all documentation in the code as comments. I intend to
purge it in favour of the green nagbar help topics.

- **$HOME $USER** Fix numerous hardcoded "/home/ellathecat" strings, with sway config variables and bash
variables.

- **ShellCheck Scripts** Every script to pass ShellCheck by hand. Automation not a shipshape
requirement. Initial commit exempt.

- **One Config Review** Concatenate all configs into one, strip comments and blank lines, insert file
boundaries. Ask sway reddit how to run the nagbar validation on it.

- **About Workspaces** All the help topics to have something of substance written. The workspace related
topics need drafting.

- **Context Help** Excepting Menu Keys and More Menu Keys modes, not a shipshape requirement beyond an
empty document with the correct title for the current mode. **There has to be a WASD keyboard layout
diagram** accessible (show|hide) via the keyboard for these two modes. Mod5+slash is reserved for this.

## About Us

Ella was my pet cat and the inspiration for my not-at-work alter-ego EllaTheCat on github. She is also
my presence as EllaTheCat on reddit as someone who is helpful but not afraid to show her claws. I'm Karl
Wood, the one with PD.
