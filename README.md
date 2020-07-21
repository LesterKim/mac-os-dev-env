# mac-os-dev-env
These are instructions for a basic software development environment for macOS.

### Command Line Tools
1. Install [Homebrew](https://brew.sh/).
   1. From a terminal (e.g.
   [Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)),
   run `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`.
1. [Install OhMyZsh](https://ohmyz.sh/#install).
1. [Set up git](https://docs.github.com/en/github/getting-started-with-github/set-up-git#setting-up-git).
   1. Install git by installing the XCode Command Line tools.
      1. Run `xcode-select --install`.
   1. If necessary, create a [GitHub](http://github.com/) account.
1. [Install the Node version manager n](https://www.npmjs.com/package/n#installation).
   1. Run `brew install n`.
1. Install [pyenv](https://github.com/pyenv/pyenv/).
   1. Install the [suggested build environment](https://github.com/pyenv/pyenv/wiki#suggested-build-environment).
      1. Run `brew install openssl readline sqlite3 xz zlib`.
      1. If you see an error that your `/usr/local/lib/pkgconfig` directory is not writable by your user,
      you should change ownership of the directory to your user by running
      `sudo chown -R $(whoami) /usr/local/lib/pkgconfig`. If your user needs write permission, run
      `chmod u+w /usr/local/lib/pkgconfig`.
   1. Use [`pyenv-installer`](https://github.com/pyenv/pyenv-installer) to install pyenv.
      1. Run `curl https://pyenv.run | bash`.
   1. Configure `.zshrc`.
      1. Run `echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc`.
      1. Run `echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc`.
      1. Run `echo 'eval "$(pyenv init -)"' >> ~/.zshrc`.
      1. Run `echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc`.
      1. Run `exec "$SHELL"` or restart your terminal.

### Desktop Applications
1. Install [Slack](https://slack.com/downloads/mac).
1. Install [Zoom](https://zoom.us/download).
1. Install [Docker](https://docs.docker.com/get-docker/).
1. Install [Neo4j](https://neo4j.com/download/).
1. (Optional) Install [PyCharm](https://www.jetbrains.com/pycharm/download).
   1. Ask VP of Engineering for PyCharm license.
1. (Optional) Install [iTerm2](https://www.iterm2.com/downloads.html).
1. (Optional) Install [Sublime Text 3](https://www.sublimetext.com/3).
