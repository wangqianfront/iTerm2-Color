## ZModem integration for iTerm 2

Setup
-----

0. Install lrzsz on OSX: `brew install lrzsz`
1. Save the `iterm2-send-zmodem.sh` and `iterm2-recv-zmodem.sh` scripts in `/usr/local/bin/`
2. Set up Triggers in iTerm 2 like so:

<pre>
    Regular expression: rz waiting to receive.\*\*B0100
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-send-zmodem.sh
    Instant: checked

    Regular expression: \*\*B00000000000000
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
    Instant: checked
</pre>

To send a file to a remote machine:

1. Type `rz` on the remote machine
2. Select the file(s) on the local machine to send
3. Wait for the coprocess indicator to disappear

The receive a file from a remote machine

1. Type `sz filename1 filename2 … filenameN` on the remote machine
2. Select the folder to receive to on the local machine
3. Wait for the coprocess indicator to disappear


## Honukai theme and colors for Oh My ZSH and iTerm 

![](https://raw.githubusercontent.com/oskarkrawczyk/honukai-iterm/master/honukai.png)

[See how it looks with blur and transparency](https://v.usetapes.com/SDGzCBkHh4) (video).

## Installation

### Theme

The theme is based on the wonderfully made [ys](https://github.com/robbyrussell/oh-my-zsh/blob/master/themes/ys.zsh-theme) theme from the official [oh-my-zsh repo](https://github.com/robbyrussell/oh-my-zsh).

1. Drop [`honukai.zsh-theme`](https://raw.githubusercontent.com/oskarkrawczyk/honukai-iterm/master/honukai.zsh-theme) into the `~/.oh-my-zsh/themes/` directory
2. Change the theme variable name to `ZSH_THEME="honukai"` in `~/.zshrc`
3. Reload ZSH with `source ~/.zshrc`

### Colors

1. Open **Preferences** pane on the **Profiles** tab in iTerm
2. Switch to the **Colors** tab and import the [`honukai.itermcolors`](https://raw.githubusercontent.com/oskarkrawczyk/honukai-iterm/master/honukai.itermcolors) (drop-down in the lower right corner)

**NOTE**: You'll need at least iTerm2.9-nightly (aka 3.0)
