# home-remote

Order of Calls
1. Vue Webapp on `http://<ip>:8080/remote-shell-fe/`
* calling Express `http://<ip>:3000[on|off]`
2. Express
* execute `./on.sh` or `./off.sh`
3. shell command gets executed

## Vue Webapp
`/var/www/remote-shel.fe`

vue.js app to have the button app and styling

## Express
`/var/www/express-shell-example`
listen on port 3000

express app to execute on.sh and off.sh
uses "Receiver Demo" `~/Documents/raspberry-remote/send` with argument
`11111 4 1` or `11111 4 0 ` to turn on or off

## Receiver Demo
`/home/pi/Documents/raspberry-remote`

contans the send script

## Autostart
add command 
`/var/www/express-shell-example node index.js`
to `/etc/rc.local`
