def processor_architecture
  host_arch = `uname -m`.strip
  case host_arch
  when /x86_64|amd64|i\d86/ # Intel or AMD
    "Intel"
  when /arm64|aarch64/ # ARM
    "ARM"
  else
    "Unknown"
  end
end
##
# Preflight
##

# Tap homebrew
tap 'superbrothers/zsh-kubectl-prompt'
tap 'argoproj/tap'
tap 'minamijoyo/tfmigrate'
tap 'chef/chef'
tap 'weaveworks/tap'
tap 'derailed/k9s'
tap 'aws/tap'
tap 'sqitchers/sqitch'
tap 'instrumenta/instrumenta'


##
# Browsers
#
##

# Firefox web browser
cask 'firefox' unless File.directory?('/Applications/Firefox.app')

# Firefox developer edition, which features programming tools.
cask 'firefox@developer-edition' unless File.directory?('/Applications/Firefox Developer Edition.app')

# Google Chrome web browser

cask 'google-chrome' unless File.directory?('/Applications/Google Chrome.app')

cask 'spotify'

cask 'postman'

cask 'kindle'
##
# Terminals
##
brew 'tmux'
cask 'iterm2'
##
# Shells
#
##
brew 'zsh'
brew 'z'
brew 'zsh-syntax-highlighting'
brew 'zsh-autosuggestions'
brew 'zsh-kubectl-prompt'

cask 'powershell'

cask 'keybase'
##
# Planning
#
##
cask 'notion' unless File.directory?('/Applications/Notion.app')

### Messaging
cask 'slack' unless File.directory?('/Applications/Slack.app')

##
# Editors
#
# We typically use command line editors (vim, emacs, etc.)
# and sometimes use GUI editors (atom, sublime, etc.)
##
# Vim editor
brew 'vim'

# Neovim
brew 'neovim'

cask 'visual-studio-code'
cask 'intellij-idea'

##
# Platforms
##

# Azure by Microsoft
brew 'azure-cli'
brew 'awscli'
brew 'ec2-instance-selector'
brew 'gimme-aws-creds'
cask 'google-cloud-sdk'

## Virtual machines

# Packer helps build automated machine images
brew 'packer'

# VirtualBox creates and configures portable development environments, by Oracle.
if processor_architecture == "Intel"
  cask 'virtualbox'
elsif processor_architecture == "ARM"
  cask 'virtualbox-beta'
end

# Vagrant lightweight, reproducible, portable development environments
cask 'vagrant'
cask 'vagrant-manager'
cask 'parallels'
## Provisioning

# Terraform common configuration to launch infrastructure.
brew 'tfenv'
brew 'tgenv'
brew 'terraform-docs'
brew 'tfmigrate'
brew 'tflint'
brew 'terrascan'

brew 'pre-commit'
brew 'gawk'
brew 'tfsec'
brew 'coreutils'
brew 'checkov'

brew 'conftest'
brew 'opa'
cask 'inspec'

brew 'kubectl'
brew 'kubeval'
brew 'eksctl'
brew 'octant'
brew 'k9s'
brew 'helm'
brew 'argocd'

brew 'minikube'
brew 'kind'

brew 'stern'
brew 'velero'
cask 'lens'

brew 'act' # https://github.com/nektos/act
brew 'k6'

## Configuration management

# Ansible is a simple way to automate apps and IT infrastructure.
brew 'ansible'

brew 'stow'
brew 'reattach-to-user-namespace'
brew 'htop'

# Jsonnet is a DSL for json
brew 'jsonnet'
brew 'wget'

brew 'gh'

# Node version manager
brew 'n'
brew 'yarn'
brew 'jabba'

brew 'go'

cask 'dotnet-sdk'

brew 'maven'

brew 'scalaenv'
brew 'sbtenv'
brew 'mill'

brew 'pyenv'
brew 'poetry'
# FZF is a command line fuzzy finder
brew 'fzf'
brew 'jq'
brew 'yq'

brew 'hugo'

brew 'graphviz'

brew 'corkscrew'
brew 'gettext' # envsubst, etc

##
# Server-Related
##

# Docker software containers to help distribute applications.
brew 'docker'
brew 'docker-compose'
brew 'colima'


## Containeriztion

# Docker assembles applications from components.
brew 'dive'
brew 'podman'

brew 'whalebrew'

## Security
cask '1password'
cask '1password-cli'
brew 'gpg'
brew 'sops'

##
# Data
##
cask 'dbeaver-community'
brew 'cpanminus' # required for sqitch
brew 'unixodbc'
cask 'snowflake-snowsql'
# disable sqitch until https://github.com/sqitchers/homebrew-sqitch/issues/56 is fixed
# brew 'sqitch', args: ['with-postgres-support', 'with-sqlite-support', 'with-snowflake-support']

###########################################################################
#
# FONTS
#
###########################################################################

##
# Fonts
##

cask 'font-3270'
cask 'font-hack-nerd-font'
cask 'font-jetbrains-mono-nerd-font'
