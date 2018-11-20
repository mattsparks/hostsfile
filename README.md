# hostsfile
Have you grown weary of working with your `hosts` file? Are you tired of editing it in your editor of choice? Look no further, traveler! _hostsfile_ is a tool to elevate your suffering.

Want to add a domain to your hosts file? Easy!

```shell
sudo hostsfile add 127.0.0.1 example.com
example.com added to hosts file!
```

Change your mind? You always were unpredictable!

```shell
sudo hostsfile remove example.com
example.com removed from hosts file!
```

Maybe you'd like only to pause your addition...

```shell
sudo hostsfile pause example.com
example.com paused!
```

But wait! Let's let it live again!

```shell
sudo hostsfile resume example.com
example.com resumed!
```

# Installation

These instructions are for macOS. The script should work on most Linux distributions, but hasn't been tested.

For those of you that use bash scripts regularly, I'll assume you have a directory somewhere with your scripts. Just add `hostsfile` to your directory, give it the proper permissions, and you should be good to go.

Follow along below if you're new to bash scripts or need a little refresher. This is adapted from the wonderful tutorial from Tania Rascia called [How to Create and Use Bash Scripts](https://www.taniarascia.com/how-to-create-and-use-bash-scripts/).

1. Open your terminal.

2. Create a `bin` directory in your home directory.

```shell
cd ~
mkdir bin
```

3. Export your bin directory.

```shell
sudo nano ~/.bash_profile # open .bash_profile
```
Add the following line:

```shell
export PATH=$PATH:/Users/your_user/bin
```
Be sure to replace "your_user" with your directory name.

Exit nano `CRTL+X` and save.

4. Clone this repo and copy the `hostsfile` to your `/bin` directory.

```shell
cd ~/Code # navigate somewhere other than /bin
git clone https://github.com/mattsparks/hostsfile.git
cd hostsfile
cp hostsfile /Users/your_user/bin/hostsfile
```

5. Make it executable.

```shell
cd ~/bin # navigate to your bin if you're not there
chmod u+x hostsfile
```

# Contribute

I have **zero** doubt that this code can be improved. I'd love your contribution!

1. Fork this repo.
2. Create a new branch.
3. Send pull request.