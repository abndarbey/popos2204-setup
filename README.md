# Pop OS Packages Setup Commands

## Golang setup with [Gobrew](https://github.com/kevincobain2000/gobrew)

#### *Step 1 - Install*
```bash
$ curl -sLk https://git.io/gobrew | sh -
```

#### *Step 2 - Set Path in `.bashrc` or `.profile` file*
```bash
export PATH="$HOME/.gobrew/current/bin:$HOME/.gobrew/bin:$PATH"
```

#### *Step 3 - Use gobrew commands to setup specific version of go*
```bash
gobrew ls-remote
gobrew use 1.16
gobrew ls
gobrew uninstall 1.16
go version
```