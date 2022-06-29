## !! THIS GUIDE IS WIP !!

# The X Binary Package System / XBPS
### What is XBPS?
The X Binary Package System (in short XBPS) is a binary package system designed and implemented from scratch. Its goal is to be fast, easy to use, bug-free, featureful and portable as much as possible.

## Commands
The XBPS isn't a standalone command, there's actually multiple commands for XBPS. These are the ones you probably going to use the most:

- xbps-install - Install
- xbps-remove - Remove
- xbps-query - Search
- xbps-reconfigure - Configure

## Examples

### System Upgrade
`$ xbps-install -Suy`

|  Needs Root permissions? | YES  |
| ------------ | ------------ |

<br>
The `-S` options means sync, or in other words: install.
<br>
The `-u` option means upgrade
<br>
The `-y` option means yes. The script won't ask you any questions, going to do all things automatically. Isn't required, but may be useful when you're upgrading your system after a long time, so you just use the `-y` option and walk away.

### System Update
`$ xbps-install -S`

|  Needs Root permissions? | YES  |
| ------------ | ------------ |

<br>
Updates the repositories, on example: When you install `void-repo-multilib` for more software available, you HAVE to run the `$ xbps-install -S` command so you update the repository and the xbps adds more software to install...

### Remove package(s)
`$ xbps-remove -R package`

|  Needs Root permissions? | YES  |
| ------------ | ------------ |

<br>
The `-R` options means remove
<br>
If you don't specify the `-R` option, no dependencies that relies ONLY on that specific packages WON'T be removed.
<br>
You can also add the `-y` option we mentioned earlier

### Remove orphans
`$ xbps-remove -o`

|  Needs Root permissions? | YES  |
| ------------ | ------------ |


<br>
If you forgot to add the `-s` option when removing some package, you can run `$ xbps-remove -o` to remove unused dependencies manually. Useful when you want to clean up your system.

### Search for packages
`$ xbps-query -Rs package`

|  Needs Root permissions? | NO  |
| ------------ | ------------ |

The `-Rs` option will search for all packages, that has `package` in it's name.
Packages will have **[*]** or **[-]** before their name. The **[*]** means that you have the package installed, the **[-]** means you don't.
<br>

### System Configuration
`$ xbps-reconfigure -f fontconfig`

|  Needs Root permissions? | YES  |
| ------------ | ------------ |

<br>
The `-f` option means Force, so it tries to execute that command whatever it takes, might be dangerous if you don't know what you're doing. But in this case, we are just forcing the update of font configuration, on example: When you install new fonts or configure an existing one, you can use this command to apply the changes.



