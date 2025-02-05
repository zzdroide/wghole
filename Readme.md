# WireGuard Hole

Pi-Hole with WireGuard, to block ads on iOS.

_Adapted from https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Pi-Hole_

To block ads, I use:
- for PC: [uBlock Origin](https://ublockorigin.com/)
- for Android: [AdAway](https://adaway.org/)
- for iOS: this repo :)

## Setup

Requirements: docker, git

1. `git clone https://github.com/zzdroide/wghole && cd wghole`
2. Copy `.example.env` to `.env` and edit its values
3. `docker compose up -d`
4. Log into wg-easy at http://localhost:8173. If you are using a web browser in your PC, forward the port from your server with `ssh -NL 8173:127.0.0.1:8173 user@server`
5. Add a new client, then click the QR button to show the configuration
6. On your iDevice, [install WireGuard](https://apps.apple.com/us/app/wireguard/id1441195209), open it, tap `+` and choose _Create from QR code_

## Usage

To add more devices, on your device with active VPN you can access wg-easy at http://10.172.1.2. You can also access Pi-Hole configuration at http://pi.hole
