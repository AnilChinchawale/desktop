# Musicoin Desktop ![Version Info](https://img.shields.io/badge/version-0.70-%23ffff00.svg)

The official Musicoin Wallet

# Running on Ubuntu (for Window/Mac, just download, unzip and run up Musicoin-wallet)

1. Download wallet: https://github.com/Musicoin/desktop/releases (find the latest version for Linux)
2. Unzip the tar file
3. Open terminal in the root folder of the MusiCoin folder
4. run `sudo linux-setup.sh` (requires root privileges) and install any missing libraries
5. type ./Musicoin-wallet and hit enter
6. Enjoy [MUSIC](https://musicoin.org/welcome)

# Build from scratch

1. Download or Clone this repository
2. Install NodeJS packages: `npm install`
3. Install bower: `npm install -g bower`
4. Install bower packages: `bower install` Note: If this doesn't work, try manually navigating to `/interface` and then try running `bower install`
5. Download the SDK version of [nw.js](http://nwjs.io/), install it and put it into executable `PATH`


# Running the App

1. Start [gmc](https://github.com/Musicoin/go-musicoin) `gmc --rpc --rpcapi="db,eth,net,web3,personal" --rpcport "8545" --rpcaddr "127.0.0.1" --rpccorsdomain "localhost"`
2. Start IPFS: `ipfs daemon`
3. Run `nw .` in the root of the repo. Note: If you're on macOS/OSX, you wouldn't be able to setup `nw` courtesy [this bug](https://github.com/nwjs/npm-installer/issues/56). In this case, download `nwjs@0.20.0` for testing

# Packaging the App

1. Install nwjs-builder: `npm install nwjs-builder -g`
2. Package the app: `nwb nwbuild -v 0.17.4 -p win64,osx64,linux64 -o build --side-by-side`
3. Update `geth` and `ipfs` executables for each platform. See links below for obtaining the files

# Packaging Dependencies

If you have the dependencies ready to go in a directory, you can just copy them into the bin directory generated by the builder command. In this example, the builder was given an output folder of `C:\tmp\mc-mvp3`, and the dependencies are stored in `C:\tmp\mc-mvp3\dependencies\`. Clearly a build script is needed...

```
robocopy C:\tmp\mc-mvp3\dependencies\win64 C:\tmp\mc-mvp3\Musicoin-wallet-win-x64\bin /S
robocopy C:\tmp\mc-mvp3\dependencies\osx64 C:\tmp\mc-mvp3\Musicoin-wallet-osx-x64\bin /S
robocopy C:\tmp\mc-mvp3\dependencies\linux64 C:\tmp\mc-mvp3\Musicoin-wallet-linux-x64\bin /S
```

# Screenshots

![image](https://github.com/Musicoin/desktop/blob/master/images/1.png) ![image](https://github.com/Musicoin/desktop/blob/master/images/2.png)

# Contributing

Pull Requests and Bug Reports for common issues via GitHub are most welcome. For security related issues however, please do not open a GitHub Issue and send a brief report over to `team@musicoin.org` with the concerned details, we shall award you with a bounty as per the bounty program guidelines.

# Bounty program

Information regarding the bounty program can be found over at BOUNTY.md.

# Additional Resources

## Builds for IPFS

<https://ipfs.io/docs/install/>

## Builds for Blockchain - gmc

<https://github.com/Musicoin/go-musicoin>
