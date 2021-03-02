# made

Mac Automated Development Environment



1. Install Xcode Command Line Tools.
    ```bash
    xcode-select --install
    ```

2. Setup homebrew & ansible.
    ```bash
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    brew update -v && brew upgrade -v
    brew install python3
    pip3 install ansible --user
    ~/Library/Python/$(python3 --version|awk {'print substr($2,1,3)'})/bin/ansible-playbook -c local -i hosts main.yml --ask-become-pass
    ```


----
