# [Vaultwarden](https://github.com/dani-garcia/vaultwarden)

A Proxmox VM running Ubuntu 22.04 LTS

## Why

I want to be in control of my passwords and not rely on a cloud solution. I previously used LastPass but got fed up with having to either pay or only use it on mobile or desktop.

## Building from source

Followed the Wiki [here](https://github.com/dani-garcia/vaultwarden/wiki/Building-binary)

1. Install dependencies required to build the binaries: `build-essential`, `git`, `pkg-config` and `libssl-dev`
   - I'm gonna use MySQL so I'll also install `libmariadb-dev-compat`, `libmysqlclient-dev` and `libmariadb-dev`
   - Make sure MySQL is installed and setup securely
   - We also need NodeJS and Rust Nightly so I'm going to install NodeJS with [NVM](https://github.com/nvm-sh/nvm) and Rust with [rustup](https://rustup.rs/)
2. Clone the [Vaultwarden](https://github.com/dani-garcia/vaultwarden) repository and `cd` into that directory
3. Copy the `.env.template` to `.env`
4. Edit the `.env` as needed, this is the config for Vaultwarden so take your time and ensure your configuration is correct
5. Build Vaultwarden with `cargo build --features mysql --release`
6. Congrats, you should now have a working Vaultwarden Backend build.. now for the Web Vault
7. Grab a pre compiled frontend from [here](https://github.com/dani-garcia/bw_web_builds/releases)
8. Uncompresss it with `tar -xvzf whatever.tar.gz`
9. You can now run the `vaultwarden` binary and access the web vault at http://localhost:8000 

## Notes
