# fivem-checker [![Release](https://img.shields.io/badge/Release-V%201.0-blue)](https://github.com/clementinise/fivem-checker/releases/latest)

## WHAT IS FIVEM-CHECKER?
**FiveM Checker is a Resource that uses HTTPs Request to know if resources are outdated or not.**

*(They need to be compatible with fivem-checker, more info below)*

![image](https://user-images.githubusercontent.com/35346472/148899380-0f869376-9521-49d5-85a0-bfefc263891a.png)

<details>
  <summary>List of already compatible resources</summary>

  - [kc-test](https://github.com/clementinise/kc-test)
  - [kc-unicorn](https://github.com/clementinise/kc-unicorn)
  - [kc-carseat](https://github.com/clementinise/kc-carseat)
  - [fivem-vehicleloader](https://github.com/clementinise/fivem-vehicleloader)

</details>

Some new features will be added soon:  Command to check for updates (instead of having to restart the resource or the server), Auto-Updater, Update checker for non-compatible resources, etc

**KNOWN BUG :** 
* None (For now I guess?)

---

## HOW DOES IT WORK?? (Devs)

### First step
**You will need to add several Metadata into your `fxmanifest.lua` files, tho, the Metadata `fivem_checker` is required to make your resource compatible with this checker.**
| Manifest Metadata | Required/Optional | Description | Example |
|-|-|-|-|
| fivem_checker | Required | Without this metadata, the checker won't be able to "see" your resource | `fivem_checker 'yes'` |
| github | Required | Link to the GitHub repo of your resource | `github 'https://github.com/clementinise/kc-test'` |
| version | Required | Version of your resource (You will need to change this everytime you release an update) | `version '1.0'` |
| name | Optional | Name of your resource [(You can also use color code)](https://pastebin.com/kQdX2JVy) | `name '^2Test Script'` |

### Second step
**You will also need to add a file labeled `version` [*(An example can be found here)*](https://github.com/clementinise/kc-test/blob/main/version) in your GitHub repo**

This file need to respect certains syntax:
| Syntax | Required/Optional | Description | Example |
|-|-|-|-|
| `<version-number>` | Required | The version needs to be in between angle brackets | `<1.1>` |
| `- Changelog` | Optional | Each line of the changelogs needs to be separated by a minus symbol | `- This is a test sentence` |

### Last step

**There isn't, only those 2 steps are required to make your resource compatible with this resource 👍**

---

## INSTALLATION (Users)
Download the [latest release](https://github.com/clementinise/fivem-checker/releases/latest).

Drag the folder into your `<server-data>/resources` folder
Add this in your `server.cfg`:
```
ensure fivem-checker
```
*Note: This needs to be added at the end of your resources list in ``server.cfg``*
