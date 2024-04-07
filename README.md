# OpenVPN on your own server

## Steps to set-up
- clone this repository
- cd into repo folder
- run `docker compose up -d`

Once image is built and container started you can download client configuration:
- run `docker compose exec -it dockovpn bash` to enter container's bash
- run `wget -O client.ovpn localhost:8080` to download client details
- print file content `cat client.ovpn`, copy printed text and save it in eg. `client.ovpn` file on your computer
- remove file `rm client.ovpn`
- run `exit` to return to OS terminal

## Connect from iOS (iPhone or iPad):

Install **[OpenVPN Connect](https://apps.apple.com/pl/app/openvpn-connect-openvpn-app/id590379981)** app.
Copy your **client.ovpn** file to device, from **Files** app share it to **OpenVPN Connect** app. Follow in app steps to create new profile.


### Shortcut to turn VPN on/off
*On iOS there is no option to add VPN toggle to control center, but you can use Shortcut and save it on Home Screen.*

- Open Shortcuts app, click **+** (plus/add) icon.
- Search for VPN and add **Set VPN** action.
- Change action to *Toggle*, change *VPN* to profile created in previous steps.
- Customize name and icon to your liking.

Once done go back to Shortcuts main screen, long press new shortcut and select *Add to Home Screen*.

Done.
