#!/bin/sh

if [ ! -e install_homebrew.rb ]; then
    echo "About to download the homebrew installer."
    curl --fail --silent --show-error --location \
         https://raw.githubusercontent.com/Homebrew/install/master/install \
         -o install_homebrew.rb || exit
fi

echo "About to run the homebrew installer."
echo "This may install the Command Line Tools, if not already present."

read -p "Continue? [y/n] " -t60 -n1 -s CONTINUE

if [ ${CONTINUE} = "y" ]; then
    echo "Running homebrew installer"
    ruby install_homebrew.rb

    echo Installing ansible...
    brew install ansible
fi
