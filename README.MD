# LinuxBoxSetup
Install git:

    sudo apt install git
    git config --global user.email "email@place.com"
    git config --global user.name "Freddy Flintstone"
    git config --global credential.helper store


Install spacemacs:

  sudo add-apt-repository ppa:kelleyk/emacs
  sudo apt-get update
  sudo apt-install emacs26
  git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d

  emacs -nw

# Setup basic build tools
  sudo apt-get -y install build-essential
  sudo apt-get -y install autoconf
  sudo apt-get -y install m4
  sudo apt-get -y install libncurses5-dev
  sudo apt-get -y install libwxgtk3.0-dev libgl1-mesa-dev libglu1-mesa-dev libpng3
  sudo apt-get -y install libssh-dev
  sudo apt-get -y install unixodbc-dev
  sudo apt-get install xsltproc fop
  sudo apt install automake

# Install 'asdf' itself
  git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.2.1
  echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.bashrc
  echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bashrc

# Activate in current shell
  $HOME/.asdf/asdf.sh

# Add Elixir plugin
  asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang.git
  asdf plugin-add elixir https://github.com/asdf-vm/asdf-elixir.git

# Install Elixir 1.8 & make it global default
  asdf install erlang 21.2
  asdf global erlang 21.2
  asdf install elixir 1.8.0
  asdf global elixir 1.8.0
