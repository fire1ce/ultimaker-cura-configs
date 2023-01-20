# ultimaker-cura-configs

## App Shortcut

Cura.app is a shortcut to the Ultimaker Cura application. It is located in the Applications folder.

copy the Cura.app to your Applications folder and you can launch it from there.

## Presist Settings and Profiles with Dropbox

The Ultimaker Cura application stores settings and profiles in the following locations:

```shell
/Users/${USER}/Library/Application\ Support/cura/
```

### Initial (first time) Backup Setup

First time creating a backup, you need to copy the entire folder to your Dropbox folder.

```shell
cp -R /Users/${USER}/Library/Application\ Support/cura/ /Users/${USER}/Dropbox/SettingsConfigs/cura/
```

### Linking Dropbox to Cura

For fresh install we want to link the Dropbox's Cura settings folder to the Cura application's settings folder.

first, we need to remove the Cura application's settings folder. Then create a symbolic link to the Dropbox's Cura settings folder.

```shell
rm -rf /Users/${USER}/Library/Application\ Support/cura/
ln -s /Users/${USER}/Dropbox/SettingsConfigs/cura/ /Users/${USER}/Library/Application\ Support/cura/
```
