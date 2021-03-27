# Convert all images in a folder to WEBP

## 1. Install Google's WEBP

Get more informations at <https://developers.google.com/speed/webp/docs/precompiled>

```sh
brew install webp
```

## 2. Download the application to your `bin` folder and make it executable

Use `wget`:

```sh
wget -O /usr/local/bin/convert-to-webp https://raw.githubusercontent.com/mheob/convert-to-webp/main/convert-to-webp && \
chmod +x /usr/local/bin/convert-to-webp
```

Or use `curl`:

```sh
curl -o /usr/local/bin/convert-to-webp https://raw.githubusercontent.com/mheob/convert-to-webp/main/convert-to-webp && \
chmod +x /usr/local/bin/convert-to-webp
```

## 3. Call the script from the folder you want to store the new files

The files where always stored in the directory you are in!
You can check your current working directory with the `pwd` command.

```sh
# The easiest one
convert-to-webp

# Show the help
convert-to-webp -h
convert-to-webp --help

# Specify the quality (default 70)
convert-to-webp -q 60
convert-to-webp --quality 80

# Specify the destination folder directly
convert-to-webp . # for current folder
convert-to-webp ./images # for the subfolder "images"
convert-to-webp ../images # for the folder "images" in the current neighbor directory
convert-to-webp ~/Downloads # for the "Downloads" folder in your "HOME" directory

# Combine the quality and the destination
convert-to-webp -q 50 ~/Downloads # converts from "~/Downloads" with the quality of 50%
```

## Optional: Create an BASH or ZSH alias

In your `.bash_aliases` or `.zshrc` add for example

```sh
alias ctw="convert-to-webp"
```

Of course you can choose what ever you want.
