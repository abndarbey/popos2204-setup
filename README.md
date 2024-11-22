# Pop OS Packages Setup Commands

## Golang setup with [Gobrew](https://github.com/kevincobain2000/gobrew)

#### *Step 1 - Install*
```bash
curl -sL https://raw.githubusercontent.com/kevincobain2000/gobrew/master/git.io.sh | bash
```

#### *Step 2 - Set Path in `.bashrc` or `.profile` file*
```bash
export PATH="$HOME/.gobrew/current/bin:$HOME/.gobrew/bin:$PATH"
```

- ignore the below commands
```
export PATH="$HOME/.gobrew/current/bin:$HOME/.gobrew/bin:$PATH"
export GOROOT="$HOME/.gobrew/current/go"
```

#### *Step 3 - Use gobrew commands to setup specific version of go*
```bash
gobrew help
gobrew ls-remote # list all the available remote versions of go for installation
gobrew use 1.22.2 # install and set a specific version of go
gobrew install 1.22.2 # install a specific version of go
gobrew ls # list all the available versions of go in the system
gobrew uninstall 1.22.2 # uninstall a specific version of go
go version # verify the version of golang in the system
```

<hr>

## NodeJS setup with [NVM](https://github.com/nvm-sh/nvm#install--update-script)

#### *Step 1 - Install*
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

#### *Step 2 - Set Path in `.bashrc` or `.profile` file*
```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

#### *Step 3 - Use nvm commands to setup specific version of go*
```bash
nvm --version
nvm ls-remote
nvm use 20
nvm ls
nvm uninstall 20
node --version
npm --version
```

## neofetch, cpufetch, gdu setup

#### *neofetch setup*
```bash
sudo apt install neofetch
neofetch
```

#### *cpufetch setup*
```bash
sudo apt install cpufetch
cpufetch
```

#### *gdu setup*
```bash
sudo apt install gdu
gdu
gdu -h
```
