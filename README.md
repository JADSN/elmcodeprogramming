# elmcodeprogramming
Elm setup and codes

# SETUP

Setup for woking with [Elm](https://elm-lang.org/).

## Setup

---
### **Linux**
1. Install GNU/Linux (Debian Stable or Ubuntu LTS 20.04)
1. `sudo apt-get install pkg-config build-essential docker.io git curl code -y`

---
#### **Visual Studio Code**

1. `code --install-extension aaron-bond.better-comments`
1. `code --install-extension usernamehw.errorlens`
1. `code --install-extension yzhang.markdown-all-in-one`
1. `code --install-extension Elmtooling.elm-ls-vscode`
1. `code --install-extension joaompinto.vscode-graphviz`
1. `code --install-extension EFanZh.graphviz-preview`

```bash

cat > $HOME/.config/Code/User/settings.json <<EOF
{
    "editor.bracketPairColorization.enabled": true,
    "editor.guides.bracketPairs": "active",
    "editor.fontSize": 14,
    "editor.fontWeight": "bold",
    "editor.formatOnSave": true,
}
EOF

```

### **Git**
1. In github menu go to:
   1. Settings  
   1. Email
   1. Enable the option: **Keep my email addresses private** 
1. `git config --global core.editor code`
1. `git config --global --edit`
1. Paste in `.gitconfig` file
```bash
[user]
	name = <git_username>
	email = <email_noreply>
[core]
	autocrlf = input
	editor = code
```

---
### **Docker**

1. `sudo groupadd docker`
1. `sudo usermod -aG docker $USER`
1. `newgrp docker`  
1. `docker run hello-world`

---
### **NodeJs using nvm**
1. [Install nvm](https://github.com/nvm-sh/nvm)
1. `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
1. `export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"`
1. `[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm`
1. `nvm install 16` --> **Observation: In node v.17 doesn't work crate-elm-app package**
1. `nvm use 16`
1. `npm install -g elm elm-test elm-format elm-test elm-format elm-review create-elm-app uglify-js`

---
### **Elm**
1.  `elm --help`
1. `create-elm-app <app_name>`
1. `cd <app_name>`
1. `elm-app start` 
1. `elm install mdgriffith/elm-ui`

---
### **SSH**

1. `ssh-keygen -t ed25519 -C "email"`
1. In github menu go to:
   1. Settings  
   1. SSH and GPG Keys
   1. New SSH Key
   1. Paste the content of the file `~/.ssh/id_ed25519.pub`
   1. git clone `<repo_url>`
   1. If propmt some message type **yes**

