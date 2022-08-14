# arch-windows

A handy Docker Compose configuration and scripts to run an Arch Linux shell on Windows

## Prerequesites

You need to have [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/) (and [WSL](https://docs.microsoft.com/en-us/windows/wsl/install)) installed before using  

## How to Use

### Opening a Shell

Simply run the `.\bash.bat` and a bash shell will open up. Type `exit` from within the shell to go back into PowerShell/Command Prompt (depending on what you've done in the shell, you might need to type `exit` multiple times). It'll automatically stop the container when you do this, just make sure to allow enough time for it to gracefully stop.

## Volumes

There should be a `data` folder created after you run the `bash.bat` script. This folder corresponds to `/root/data` in the container. Note: since you're the root user in the container, `/root` acts like your home directory (`~`), so `/root/data` is like `~/data`.

## Next Steps

You're probably going to want to update your packages so you can start installing stuff:

```sh
pacman -Syu
```

To install stuff (for example, Vim), run the following:

```sh
pacman -S vim
```

## Clean Up/Deletion

If you'd like to clean up/delete everything, simply run `docker compose down`. Note: the `data` folder won't be deleted even after you do this. If you'd like to delete it, you'll need to do so manually
