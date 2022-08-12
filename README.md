# arch-windows
A handy Docker Compose configuration to run Arch Linux on Windows

## Pre Requesites

You need to have [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/) (and [WSL](https://docs.microsoft.com/en-us/windows/wsl/install)) installed before using  
## How to Use

### Starting the Container

Run `.\start.bat` to start the container. The container will now be running and you can `exec` into it.

### Opening a Shell

Simply run the `.\bash.bat` and a bash shell will open up.

### Stopping the Container

Once you're done using the container, you can stop it by running `.\stop.bat`, You will now need to run `.\start.bat` to be able to open a shell again.
## Volumes

There should be a `root` folder created after you run the `bash.bat` script. This folder corresponds to `/root` in the container. Since you're the root user in the container, this folder acts like your home directory (`~`).
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

If you'd like to clean up/delete everything, simply run `docker compose down`.