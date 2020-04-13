<p align="center">
  <img src="https://s3.amazonaws.com/ohmyzsh/oh-my-zsh-logo.png" alt="Oh My Zsh">
</p>

Oh My Zsh is an open source, community-driven framework for managing your [zsh](https://www.zsh.org/) configuration.

Sounds boring. Let's try again.

__Oh My Zsh will not make you a 10x developer...but you may feel like one.__

Once installed, your terminal shell will become the talk of the town _or your money back!_ With each keystroke in your command prompt, you'll take advantage of the hundreds of powerful plugins and beautiful themes. Strangers will come up to you in cafés and ask you, _"that is amazing! are you some sort of genius?"_

Finally, you'll begin to get the sort of attention that you have always felt you deserved. ...or maybe you'll use the time that you're saving to start flossing more often. 😬

To learn more, visit [ohmyz.sh](https://ohmyz.sh), follow [@ohmyzsh](https://twitter.com/ohmyzsh) on Twitter, and/or join us on Discord.

[![CI](https://github.com/ohmyzsh/ohmyzsh/workflows/CI/badge.svg)](https://github.com/ohmyzsh/ohmyzsh/actions?query=workflow%3ACI)
[![Follow @ohmyzsh](https://img.shields.io/twitter/follow/ohmyzsh?label=Follow+@ohmyzsh&style=flat)](https://twitter.com/intent/follow?screen_name=ohmyzsh)
[![Discord server](https://img.shields.io/discord/642496866407284746)](https://discord.gg/bpXWhnN)

## Getting Started

### Prerequisites

* A Unix-like operating system: macOS, Linux, BSD. On Windows: WSL is preferred, but cygwin or msys also mostly work.
* [Zsh](https://www.zsh.org) should be installed (v4.3.9 or more recent). If not pre-installed (run `zsh --version` to confirm), check the following instructions here: [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
* `curl` or `wget` should be installed
* `git` should be installed (recommended v1.7.2 or higher)

### Basic Installation

Oh My Zsh is installed by running one of the following commands in your terminal. You can install this via the command-line with either `curl` or `wget`.

#### via curl

```shell
sh -c "$(curl -fsSL https://github.com/lylyulei/ohmyzsh/master/tools/install.sh)"
```

#### via wget

```shell
sh -c "$(wget -O- https://github.com/lylyulei/ohmyzsh/master/tools/install.sh)"
```

#### Manual inspection

It's a good idea to inspect the install script from projects you don't yet know. You can do
that by downloading the install script first, looking through it so everything looks normal,
then running it:

```shell
curl -Lo install.sh https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

## Using Oh My Zsh

### Plugins

Oh My Zsh comes with a shitload of plugins to take advantage of. You can take a look in the [plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) directory and/or the [wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) to see what's currently available.

#### Enabling Plugins

Once you spot a plugin (or several) that you'd like to use with Oh My Zsh, you'll need to enable them in the `.zshrc` file. You'll find the zshrc file in your `$HOME` directory. Open it with your favorite text editor and you'll see a spot to list all the plugins you want to load.

```shell
vi ~/.zshrc
```

For example, this might begin to look like this:

```shell
plugins=(
  git
  bundler
  dotenv
  osx
  rake
  rbenv
  ruby
)
```

_Note that the plugins are separated by whitespace. **Do not** use commas between them._

#### Using Plugins

Most plugins (should! we're working on this) include a __README__, which documents how to use them.

### Themes

We'll admit it. Early in the Oh My Zsh world, we may have gotten a bit too theme happy. We have over one hundred themes now bundled. Most of them have [screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) on the wiki. Check them out!

#### Selecting a Theme

_Robby's theme is the default one. It's not the fanciest one. It's not the simplest one. It's just the right one (for him)._

Once you find a theme that you'd like to use, you will need to edit the `~/.zshrc` file. You'll see an environment variable (all caps) in there that looks like:

```shell
ZSH_THEME="robbyrussell"
```

To use a different theme, simply change the value to match the name of your desired theme. For example:

```shell
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# see https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster
```

_Note: many themes require installing the [Powerline Fonts](https://github.com/powerline/fonts) in order to render properly._

Open up a new terminal window and your prompt should look something like this:

![Agnoster theme](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

In case you did not find a suitable theme for your needs, please have a look at the wiki for [more of them](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes).

If you're feeling feisty, you can let the computer select one randomly for you each time you open a new terminal window.


```shell
ZSH_THEME="random" # (...please let it be pie... please be some pie..)
```

And if you want to pick random theme from a list of your favorite themes:

```shell
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
)
```

If you only know which themes you don't like, you can add them similarly to a blacklist:

```shell
ZSH_THEME_RANDOM_BLACKLIST=(pygmalion tjkirch_mod)
```

### FAQ

If you have some more questions or issues, you might find a solution in our [FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Advanced Topics

If you're the type that likes to get their hands dirty, these sections might resonate.

### Advanced Installation

Some users may want to manually install Oh My Zsh, or change the default path or other settings that
the installer accepts (these settings are also documented at the top of the install script).

#### Custom Directory

The default location is `~/.oh-my-zsh` (hidden in your home directory)

If you'd like to change the install directory with the `ZSH` environment variable, either by running
`export ZSH=/your/path` before installing, or by setting it before the end 
