This is my global configuration for [PhpStorm](https://www.jetbrains.com/phpstorm/). PhpStorm is an IDE for PHP. I have some custom configuration for code styling, inspections and file templates, and I use
Git to track these configuration files and to synchronize them between workstations. The code style rules follow PSR-2 but I also added some things that are not specified in the PSR guidelines.

Feel free to use or fork this repository. Note: I use PhpStorm 8. These settings might work with other versions as well, but I cannot guarantee.

# Installation

Before you do this, make sure PhpStorm is not running, or it will overwrite your changes.

Use the following commands to go to the config directory, remove some default directories, and pull the files from my repository:

```bash
# replace .WebIdeXX with the actual name of the folder: .WebIde70 for PhpStorm 7, .WebIde80 for PhpStorm 8.
cd ~/.WebIdeXX/config

# remove the files and folders that are in this repository
rm -r codestyles/
rm -r fileTemplates/
rm -r inspection/

git init
git remote add origin git@github.com:nicwortel/phpstorm-ide-config.git
git fetch
git checkout -t origin/master
```

## Location of the config folder

OS | Location
---|---------
Windows XP | `C:\Documents and Settings\<User name>\.WebIdeXX\config`
Windows Vista | `C:\Users\<User name>\.WebIdeXX\config`
Linux | `~/.WebIdeXX/config`
Mac OS | `~/Library/Preferences/WebIdeXX`

See [Project and IDE settings](http://www.jetbrains.com/phpstorm/webhelp/project-and-ide-settings.html#d610183e276) for more information.

## Subdirectories of the config folder

Directory | Contents
----------|---------
codestyles | Code Style settings (Editor > Code Style)
colors | Colors & Fonts settings (Editor > Colors & Fonts)
fileTemplates | File and Code Templates (Editor > File and Code Templates)
filetypes | File Types (Editor > File Types)
inspection | Inspection profiles (Editor > Inspections)
keymaps | Keyboard shortcuts (Appearance & Behavior > Keymap)
templates | Live templates (Editor > Live Templates)
