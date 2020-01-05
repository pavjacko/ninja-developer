# USEFUL ALIASES
# Add this to one of ~/.zshrc , ~/.bash_profile , ~./bashrc depending on your setup

# Source Bash Files
alias sb="source ~/.zshrc"

# Open Chrome gmail
alias mail="/usr/bin/open -a \"/Applications/Google Chrome.app\" 'https://mail.google.com/mail/u/0/#inbox'"
alias drive="/usr/bin/open -a \"/Applications/Google Chrome.app\" 'https://drive.google.com/drive/my-drive'"

# Open Finder from current terminal path
alias f="open ."

# Open Various apps from current terminal path
alias s="sublime ."
alias v="code ."
alias a="atom ."

# Open and edit bash profile files
alias bp="atom ~/.bash_profile"
alias bb="atom ~/.bashrc"
alias bz="atom ~/.zshrc"

# DEVELOPER NOTES
alias n="atom /PATH_TO_YOUR_NOTES_FOLDER"

# NPM
alias i="npm i"
alias clean="rm -rf node_modules; rm -rf ./package-lock.json; rm -rf ./yarn.lock;"

# GIT
alias gc="git commit -a -m "
