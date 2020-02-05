# Overview

# Usage

1. Install Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2. Run homebrew bundler

```
brew bundle
```

3. Run ansible playbook
```
sudo ansible-playbook -i localhost playbook.yml --extra-vars="@secrets.yml"
```