# CosmWasmResourceBook

Blockchain technology has obviously captured the attention of a substantial number of people, some of whom are aspiring developers, a group that I belong to. But, at least for me, the learning curve is equivalent to the Mongells trying to overcome great wall of China. 
 
A little background first. I fit in the category of coders who are self-taught and as a self-taught coder there is a large void in my understanding. As an example, I have always known that development required the use of an array of interconnected frameworks that make a system function. However, what I did not know is that this was called a tech stack... 
 
So, this is a resource dedicated to these people, my people, the people like me. The large swaths of aimless souls crawling on the surface of true development. The reason for building this resource is to anchor myself. To act as a starting point for my development career, which to this point has been non-existent. 
 
Enough story telling lets get into it. 
 
Obviously the first thing is to setup the environment, lets start there. 


## Environment Setup

I will assume that because it's 2022 your setup is Windows 10/11 runing `WSL2`.
If you don't know what I'm talking about or simply wish to following along, check out the resource below before moving on.

Cooming Soon. A few resources I need to compile to make this as straight forward as possible.
* WSL2 







### WSL2 Installation

https://pureinfotech.com/install-windows-subsystem-linux-2-windows-10/







#### Basic Dependencies

Run the following commands to finish he basic dependencies.
```
# update the local package list and install any available upgrades
sudo apt-get update && sudo apt upgrade -y

# install toolchain and ensure accurate time synchronization
sudo apt-get install make build-essential gcc git jq chrony -y
```





#### SSH Setup



### Install Docker




### Install Rust

First, install rustup. 

 `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`

Once installed, make sure you have the wasm32 target:

```rustup default stable
cargo version
# If this is lower than 1.50.0+, update
rustup update stable

rustup target list --installed
rustup target add wasm32-unknown-unknown
```




### Install Go
Remove any previous Go installation (You may need to run the command as root or through sudo).
`rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.linux-amd64.tar.gz`

Next Install Go
```
wget https://golang.org/dl/go1.17.1.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.17.1.linux-amd64.tar.gz
```

After that configure your users .profile `~/.profile` by adding the following lines.
```
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
```

After making those changes run `source ~/.profile` for those changes to occur.



### Install Juno

This is taken directly from the Juno Docs - Getting Started 
https://docs.junonetwork.io/smart-contracts-and-junod-development/getting-started







 
