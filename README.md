# mac-os-dev-env
These are instructions for a basic software development environment for macOS.

### Command Line Tools
1. Install [Homebrew](https://brew.sh/).
   1. From a terminal (e.g.
   [Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)),
   run `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`.
1. Install [OhMyZsh](https://ohmyz.sh/#install).
1. Set up [git](https://docs.github.com/en/github/getting-started-with-github/set-up-git#setting-up-git).
   1. If necessary, create a [GitHub](http://github.com/) account.
   1. [Set your Git username for every repository on your computer](https://docs.github.com/en/github/using-git/setting-your-username-in-git#setting-your-git-username-for-every-repository-on-your-computer).
   1. [Set your Git email for every repository on your computer](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#setting-your-commit-email-address-in-git).
1. Install a Node version manager. Two choices are `n` and `nvm`.
   1. [n](https://www.npmjs.com/package/n#installation) installation:
      1. Run `brew install n`.
   1. [nvm](https://github.com/nvm-sh/nvm) installation:
      1. There is a guide [here](https://tecadmin.net/install-nvm-macos-with-homebrew/)
      1. Run `brew install nvm` and follow the guide to update your `.bash_profile` or similar.
   - Note that the `aliro-qn-frontend` project requires Node 13.1.0, so make sure that is installed.
1. Install the Python version manager [pyenv](https://github.com/pyenv/pyenv/).
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
   1. As an alternative to `pyenv`, [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) can be used to manage environments in a way that some people find easier to use.

### Desktop Applications
1. [Slack](https://slack.com/downloads/mac)
1. [Zoom](https://zoom.us/download)
1. [Docker](https://docs.docker.com/get-docker/)
1. (Optional) [PyCharm](https://www.jetbrains.com/pycharm/download)
   1. Ask an engineering manager (e.g. VP of Engineering) for a PyCharm license.
1. (Optional) [iTerm2](https://www.iterm2.com/downloads.html)
1. (Optional) [Sublime Text 3](https://www.sublimetext.com/3)

### References
1. [Connecting to GitHub with SSH
](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
1. [Managing Multiple Python Versions With pyenv](https://realpython.com/intro-to-pyenv/)
