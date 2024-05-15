---
layout: page
---

# MacOS installation guide
These are the steps to install all of the prerequisites on MacOS.

Expect this preparation to take about 30 minutes to complete.

## What we're installing:
We will be installing the following:
* [Homebrew](https://brew.sh/)
* [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
* A current/LTS Version of `node.js`
* a Current version of [json-server](https://www.npmjs.com/package/json-server)

## Installtion:
1. Open Terminal.app
2. Paste the following code into terminal and press enter:
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. Follow the guided process
4. Paste the following code into terminal and press enter:
```shell
brew install git node json-server
```
5. Paste the following code into terminal and press enter:
```shell
sudo npm install -g json-server
```
6. Type the following command, with your fork of the GitHub repository in the place of `{Repo}`
```shell
git clone {Repo}
```
Congrats, you're now ready to start the [test your system!](before-you-start-a-tutorial#test-your-development-system)
## Optional Install
### Postman
Many of the tutorials reference and use [Postman](https://www.postman.com/downloads/). 
The installation is guided.
If you're not sure which chip your Mac has (Intel or Apple) you can click the Apple logo on the top left of your screen,  and then click `About This Mac` to confirm.
