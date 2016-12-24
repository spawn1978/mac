# macOS Sierra v. 10.12 Setup 

## Software

### Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Mac App Store

```
brew install mas
```

#### Sign in

```
mas signin email@email.com
```

### Brewfile

```
touch Brewfile
```

```
tap 'caskroom/cask'

brew 'git'
brew 'node'
brew 'npm'

cask 'brackets'
cask 'flux'
cask 'firefox'
cask 'google-chrome'
cask 'opera'
cask 'spectacle'
cask 'sequel-pro'

mas 'Pages', id: 409201541
mas 'Slack', id: 803453959
mas 'Sip', id: 507257563 
mas 'Simplenote', id: 692867256 
mas 'Todoist', id: 585829637
mas 'Numbers', id: 409203825
```

### Preferences

#### Show Library folder

```
chflags nohidden ~/Library
```

#### Show hidden files

```
defaults write com.apple.finder AppleShowAllFiles YES
```

### GitHub

#### Generate SSH key

```
ssh-keygen -t rsa -b 4096 -C "email@email.com"
```

```
[user]
	name = First Last
	email = email@email.com
[github]
	user = username
[alias]
	a = add
	ca = commit -a
	cam = commit -am
	s = status

	pom = push origin master
	pog = push origin gh-pages
	puom = pull origin master
	puog = pull origin gh-pages
    
	cob = checkout -b
```

### SSH

```
cd ~./ssh && touch config
```

```
Host example
    HostName example.com
    User example-user
    IdentityFile key.pem
```

### Bash

```
touch .bash_profile
```

```
alias brewup='brew update; brew upgrade; brew prune; brew cleanup; brew doctor'
```

```
source ~/.bash_profile
```





