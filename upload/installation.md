# Install Ark (the Arken Command-line Client)

## (Option 1) Automatic Installation
To automatically download and install Ark to your machine you can run the following command in a terminal window.
```bash
curl -L https://arken.io/ark.sh | sh
```

#### Add Ark to your PATH (Optional)
To make Ark discoverable on your system you'll need add it to your system PATH.
If you are on Linux using bash you can do this by running,
```bash
echo "export PATH=$PATH:$HOME/.ark/bin" >> ~/.bashrc
```

And if you are on MacOS running ZSH you can do this by running,
```bash
echo "export PATH=$PATH:$HOME/.ark/bin" >> ~/.zshrc
```

## (Option 2) Install from a GitHub Release Binary
1. Head over to the [Ark GitHub repository releases](https://github.com/arken/ark/releases).
2. Copy the link to your corresponding OS and Architecture.
3. Run `sudo curl -L "PATH-TO-RELEASE" -o /usr/local/bin/ark`
4. Run `sudo chmod a+x /usr/local/bin/ark`
5. (Optional) Run `sudo ln -s /usr/local/bin/ark /usr/bin/ark`

## (Option 3) Build from Source
1. Download the Ark source code git repository by running. `git clone https://github.com/arken/ark.git`
2. Enter the repository folder by typing `cd ark`
3. Build the application by running `go build .`
4. Install the application by moving it to your bin by running, `cp ark /usr/bin/ark`
