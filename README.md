# Innotech MVP :headphones::zap:

Turn your **Raspberry Pi** into a **Bluetooth hub** to play your music through multiple bluetooth **synced** speakers 🔊🔊🔊.

1. [Requirements 📜](<#Requirements 📜>)
1. [Your path to multi-devices sound on Linux ! 🔥](./installation/README.md)
1. [Run from a fresh Raspberry install 🐍](<#Run from a fresh Raspberry install 🐍>)

## Requirements 📜
- Raspberry pi (model 3B used)
- Jack cable
- 2 speakers :
    - 1 in bluetooth mode
    - 1 in AUX mode (connected with JACK cable to the headphone output of the Raspberry)
    ![architecture](./installation/architecture.png)

## Run from a fresh Raspberry install 🐍
```bash
# install innotech-mvp
git clone https://github.com/innotech-insa/innotech-mvp.git
sudo ./innotech-mvp/installation/install.sh
source ~/.bashrc
# install bluetool
git clone https://github.com/innotech-insa/bluetool.git
cd bluetool && sudo make install
# run
cd ~/innotech-mvp
flask run --host "$(hostname -I | cut -d ' ' -f 1)"
```