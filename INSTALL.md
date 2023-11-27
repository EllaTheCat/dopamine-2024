rm# dopamine-2024 INSTALL.md

## Status 27 November 2023

## Background

Someone who finds this repo expects to be able to build and run it. Trouble is thst I'm slowed down by
the PD, so quite some time elapsed with github being used as an offsite backup. This isn't the finished
article but it is what you need to know in order to apply this config to Sway, fire it up, evaluate it,
uninstall, and be able to restore your present config. I assume you know what to do, but not what could
possibly go wrong or waste your time.

## The 'config' file

The project resides in and beneath $XDG_CONFIG_HOME/sway, the "(suggested location)" from 'man 1
sway'. If your current config lives there it would be prudent to script backup and restore. There are
two subdirectories $XDG_CONFIG_HOME/sway/{config.d,scripts.d}, the former contains the **complete**
configuration, in sway format, in files with a ".config" extension, the latter contains helper scripts,
in 'bash' mainly but also python, in files with a '.script' extension.

Regular sway setups keep the top level config in $XDG_CONFIG_HOME/sway/config at the same level as the
diectory $XDG_CONFIG_HOME/sway/config,d, but dopamine-2024 does not; it keeps the contents of what would
normally be in in $XDG_CONFIG_HOME/sway/config in a file '000-includes.config' in
$XDG_CONFIG_HOME/sway/config.d instead.

Why? As the aforermentioned '000-includes.config' suggests, the project makes heavy use of the Sway
inclede feature, with about 30 files included in '000-includes.config'. To maintain conpatiblity
'000-includes' is made the target of a symbolic link and the origin of the link is
$XDG_CONFIG_HOME/sway/config.

Why? When doing manual file management it became all too easy to think 'config.d' contained the
**complete** configuration, thereby overlooking the contents of '$XDG_CONFIG_HOME/sway/config'. Provided
the symbolic link is present, the symbolic link method just works, but it was discovered to have further
advantages, which is why it persists even with git as a backup.

In a nushell, if your present configuration is more or less default, and anchored at
$XDG_CONFIG_HOME/sway, simply overwriting my symbolic link with your file 'config' and reloading
restores your configuration, while overwriting your file with my symbolic link and reloading restores
mine, provided of course that neither of us changes anything else. THe use of .config and .script extensions helps.

## Scripts

The dopamine-2024 helper scripts live in $XDG_CONFIG_HOME/sway/{config.d,scripts.d and their names end
in .script. Most are runtime scripts called from config, a few have a keyword {utility,overview,help} in
their names, for example the props.utility script that does a get-tree to obtain such things as the
app_id of the focused object.

The binding Mod4+Shift+Escape (or Mod4+Shift+Caps when Caps is mapped to Escape) raises a green nagbar,
On this are several help topics; click topic XYZ and the script 'XYZ.help,script' runs. the first two
lines abuse the shebang, which offends ShellCheck such that the script is loaded ino Emacs(!) whereupon
the remainder of the scrip is help for XYZ, simple text or maybe Markdown, to be read or edited. There
is context sensitive help, which provides diffeent help texts for different modes, via {ABC.DEF,...}
.help.script. The overview scripts are 60% done, the help scripts still just messing about. There are
workspace scripts that run when a workspace is visited, they're in good shape.

 Thi project uses a third party program called autotiling, (https://github.com/nwg-piotr/autotiling)
 that must keep running during the session.  Download it from githu b and install it. Take a copy and
 rename it to 'autotiling-3rd-party.script', use chmod to make it readable and executable by anyone, and
 writeable by no-one. It's important to make it clear we are using someone else's work and are using it
 as-is to avoid making programming mistakes that would reflect badly on its authors.