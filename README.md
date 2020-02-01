## BGforge multilanguage server
[![VScode marketplace](https://img.shields.io/visual-studio-marketplace/i/bgforge.bgforge-mls)](https://marketplace.visualstudio.com/items?itemName=BGforge.bgforge-mls)
<a href="https://www.patreon.com/BGforge"><img src="https://c5.patreon.com/external/logo/become_a_patron_button.png" width="100" alt="Support us on Patreon"></a>
[![Discord chat](https://img.shields.io/discord/420268540700917760?logo=discord)](https://discord.gg/4Yqfggm)

[__Features__](#features)
| [__Screenshots__](#screenshots)
| [__Install__](#installation)
| [__Configure__](#settings)
| [__Discuss__](https://forums.bgforge.net/viewforum.php?f=35)

BGforge MLS is a VScode extension adding support for [Star-Trek Scripting Language](https://falloutmods.fandom.com/wiki/Fallout_1_and_Fallout_2_scripting_-_commands,_reference,_tutorials) (`ssl`) used in Fallout 1 and 2 games, and several file formats (`d`, `baf`, `tp2`, `tra`, `2da`) used by [WeiDU](https://weidu.org/~thebigg/README-WeiDU.html) and [Infinity Engine](https://iesdp.bgforge.net), as well as [Sword Coast Stratagems Scripting Language](https://www.gibberlings3.net/forums/topic/13725-coding-scripts-in-ssl-some-lessons/) (`ssl`/`slb`).

- [Hotkeys](#hotkeys)
- [Roadmap](https://forums.bgforge.net/viewtopic.php?f=35&t=174&p=506)
- [Changelog](CHANGELOG.md)

### Features
* Syntax highlighting
* Completion
* Hovers
* Signature help
* Diagnostics

More [coming](https://forums.bgforge.net/viewtopic.php?f=35&t=174&p=506).

### Settings

This extension contributes the following settings:

* `bgforge.fallout-ssl.compile`: Path to Fallout SSL compile.exe plus compilation options.
* `bgforge.fallout-ssl.output_directory`: Where to put the compiled Fallout SSL scripts. Absolute path or relative to source directory.
* `bgforge.fallout-ssl.headers_directory`: Absolute path to directory containing Fallout headers, searched recursively.
* `bgforge.weidu.path`: Full path to WeiDU binary

#### SSL

Both Star-Trek Scripting Language and Sword Coast Stratagems Scripting Language use files with extension `ssl`. BGforge MLS defaults to Star-Trek Scripting Language (Fallout). If you need SCS Scripting Language instead, you can [set file associations](https://code.visualstudio.com/docs/languages/overview#_changing-the-language-for-the-selected-file) in VScode settings:
```json
"files.associations": {
  "*.ssl": "weidu-ssl"
}
```
This can be set globally, or per project, so you can work on both types of projects simultaneously.

### Hotkeys
* `CTRL+R`: compile (Fallout `ssl`) or parse (WeiDU `tp2`) file, [reporting errors](#error-reporting) if any.

### Installation
Search for BGforge in VScode marketplace, like any other extension. Alternatively, download the package from [Github releases](https://github.com/BGforgeNet/vscode-bgforge-mls/releases) tab and install it manually.

### Screenshots
##### Infinity Engine highlighting and completion

![infinity highlighting and completion example](resources/infinity.png)

##### Fallout highlighting and hovers

![fallout highlighting and hover example](resources/fallout.png)

##### Error reporting

![error reporting example](resources/error_reporting.png)
