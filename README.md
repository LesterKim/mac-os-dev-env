# mac-os-dev-env
These are instructions for a basic software development environment for [macOS](https://www.apple.com/macos).

### Command Line Tools
#### Basic Tools
1. Install [Homebrew](https://brew.sh/).
   1. From a terminal (e.g.
   [Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)),
   run `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`.
   1. For M1-chip MacBooks, add `eval $(/opt/homebrew/bin/brew shellenv)` to `.zshrc`.
1. Install the [GNU Privacy Guard](https://gnupg.org).
   1. Run `brew install gnupg`.
1. Set up [git](https://docs.github.com/en/github/getting-started-with-github/set-up-git#setting-up-git).
   1. If necessary, create a [GitHub](http://github.com/) account.
   1. [Set your Git username for every repository on your computer](https://docs.github.com/en/github/using-git/setting-your-username-in-git#setting-your-git-username-for-every-repository-on-your-computer).
   1. [Set your Git email for every repository on your computer](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#setting-your-commit-email-address-in-git).
   1. Configure commit signing.
      1. For [GitLab](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/#configure-commit-signing)
      1. For [GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification)
1. (Optional) Install [OhMyZsh](https://ohmyz.sh/#install).

#### Programming Languages
1. Install the [Node](https://nodejs.org/en) Version Manager [NVM](https://github.com/nvm-sh/nvm#install--update-script).
1. Install the [Python](https://www.python.org) version manager [pyenv](https://github.com/pyenv/pyenv/).
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
      1. Run `echo 'eval "$(pyenv init --path)"' >> ~/.zshrc`.
      1. Run `echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc`.
      1. Run `exec "$SHELL"` or restart your terminal.
1. Install the [Ruby](https://www.ruby-lang.org/en) Version Manager [RVM](https://rvm.io/).
   1. Install GPG keys.
      1. Run `gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`.
   1. Install RVM.
      1. Run `curl -sSL https://get.rvm.io | bash -s stable`.
1. Install [Go](https://go.dev).
   1. Follow the [Go download and installation instructions](https://go.dev/doc/install).
1. Install [Rust](https://www.rust-lang.org).
   1. Run `curl https://sh.rustup.rs -sSf | sh -s -- -y`.

#### Databases
1. Install [PostgreSQL](https://www.postgresql.org).
   1. Run `brew install postgresql`.
1. Install [Redis](https://redis.io).
   1. Run `brew install redis`.

### Desktop Applications
1. [Slack](https://slack.com/downloads/mac)
1. [Zoom](https://zoom.us/download)
1. [Docker](https://docs.docker.com/get-docker/)
1. (Optional) [JetBrains](https://www.jetbrains.com/all)
   1. Ask an engineering manager (e.g. VP of Engineering) for a JetBrains license.
1. (Optional) [iTerm2](https://www.iterm2.com/downloads.html)
1. (Optional) [Sublime Text 3](https://www.sublimetext.com/3)

### References
1. [Connecting to GitHub with SSH
](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
1. [Managing Multiple Python Versions With pyenv](https://realpython.com/intro-to-pyenv/)
