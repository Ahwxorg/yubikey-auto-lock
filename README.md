# YubiKey Auto Lock
> Automatically locking *any* system running udev on unplugging 

## Configuration

- Copy both the udev rules to the path in the repo: `/etc/udev/rules.d/<file>.rules`
- Change the user in the udev rules to your username. Of course, if you dont use ~/.local/bin/ for binaries, also change that path.
- Get the `yubikey-state`, `yubikey-lock` and `yubikey-unlock`, put them in your script folder that's mentioned in $PATH and in the `udev` files

## Current bugs:
- Sometimes after locking, unlock script throws a `[1]    11800 segmentation fault  ./yubikey-unlock`. 11800 is random.
