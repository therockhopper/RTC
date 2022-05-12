---
title: "Theme Terminal"
date: 2022-05-12T17:46:39-03:00
---

Example config for the new Windows terminal used for WSL
This sets your default shell to Ubuntu and uses the Nord color scheme with Fira Code font

profiles.json
```
{
  "$schema": "https://aka.ms/terminal-profiles-schema",

  "defaultProfile": "{2c4de342-38b7-51cf-b940-2309a097f518}",

  "profiles":
  [
    {
      // Make changes here to the powershell.exe profile
      "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
      "name": "Windows PowerShell",
      "commandline": "powershell.exe",
      "hidden": false
    },
    {
      // Make changes here to the cmd.exe profile
      "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
      "name": "cmd",
      "commandline": "cmd.exe",
      "hidden": false
    },
    {
      "guid": "{2c4de342-38b7-51cf-b940-2309a097f518}",
      "hidden": false,
      "name": "Ubuntu",
      "fontFace": "Fira Code",
      "colorScheme":"nord",
      "source": "Windows.Terminal.Wsl"
    },
    {
      "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
      "hidden": false,
      "name": "Azure Cloud Shell",
      "source": "Windows.Terminal.Azure"
    }
  ],

  // Add custom color schemes to this array
  "schemes": [
    {
      "name" : "nord",
      "background" : "#2e3440",
      "foreground" : "#d8dee9",
      "black": "#3b4252",
      "blue": "#81a1c1",
      "brightBlack": "#4c566a",
      "brightBlue": "#81a1c1",
      "brightCyan": "#8fbcbb",
      "brightGreen": "#a3be8c",
      "brightPurple": "#b48ead",
      "brightRed": "#bf616a",
      "brightWhite": "#eceff4",
      "brightYellow": "#ebcb8b",
      "cyan": "#88c0d0",
      "green": "#a3be8c",
      "purple": "#b48ead",
      "red": "#bf616a",
      "white": "#e5e9f0",
      "yellow": "#ebcb8b"
    }],

    // Add any keybinding overrides to this array.
    // To unbind a default keybinding, set the command to "unbound"
    "keybindings": []
}
```
