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

mas 'Slack', id: 803453959
mas 'Sip', id: 507257563 
mas 'Simplenote', id: 692867256 
mas 'Todoist', id: 585829637
```

### Preferences

#### Show Library folder

```
chflags nohidden ~/Library
```

### Show hidden files

```
defaults write com.apple.finder AppleShowAllFiles YES
```

### GitHub

#### Generate SSH key

```
ssh-keygen -t rsa -b 4096 -C "email@email.com"
```

```
git config --global user.name "Tania Rascia"
git config --global user.email taniarascia@gmail.com
git config --global github.user taniarascia
```
