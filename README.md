# SoftEther Configuration : کانفیگ سافت اتر


###### Video : لینک ویدیو یوتیوب
```
https://youtu.be/6oJDcVhoQz8
```

###### خرید دامنه از نیم چیپ: 
```
https://namecheap.pxf.io/BX7m6W
```
###### خرید دامنه سایت ایرانی: 
```
https://www.hub.shatelhost.com/aff.php?aff=290
```
###### خرید سرور از دیجیتال اوشن : 
```
https://m.do.co/c/0fb522deafa4
```
###### خرید سرور از سایت ایرانی : 
```
https://dashboard.azaronline.com/order/?aff=790
```

**If you think this project is helpful to you, you may wish to give a** 🌟

**Feel Free To Donation :** ❤️

>TRC20: ```TGTyqv2MH7dZztMvaP5PKuS9Bma8RY5Pk8```

>ETH: ```0x5b5202a54e5ce4fb25f0d886254eeb07bb088614```



###### Update & Upgrade Server : آپدیت و آپگرید سرور

```
sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get autoremove -y 
```

###### Install needed Package : نصب پکیجهای مورد نیاز

```
apt-get -y install build-essential wget curl gcc make wget tzdata git libreadline-dev libncurses-dev libssl-dev zlib1g-dev
```

###### Import SoftEther: ایپمورت کردن سافت اتر

```
wget https://github.com/SoftEtherVPN/SoftEtherVPN_Stable/releases/download/v4.39-9772-beta/softether-vpnserver-v4.39-9772-beta-2022.04.26-linux-x64-64bit.tar.gz
```

###### Extract SoftEther : اکسترکت کردن سافت اتر

```
tar xzf so<Press "tab" to Autofill>
```

###### Enter to Dic & Compile the SE : ورود به فولدر  و کامپایل سافت اتر

```
cd vpnserver && sudo make
```

###### Change the Dic & Permission : تغییر دایرکتوری و پرمیشن ها
```
cd ..
sudo mv vpnserver /usr/local && cd /usr/local/vpnserver/

sudo chmod 600 *

sudo chmod 700 vpnserver vpncmd
```

###### Enable & Start the SE Server : استارت وی پی ان سرور
```
sudo ./vpnserver start

sudo ./vpncmd
```
###### Set Passwd For SE Server : ست پسورد ادمین وی پی ان

```
ServerPasswordSet
```
###### Exit of managment : خروج از منیجر وی پی ان

```
exit
```


###### Create a Service : ساخت سرویس وی پی ان
```
sudo cat >> /lib/systemd/system/vpnserver.service << EOF

[Unit]

Description=SoftEther VPN Server

After=network.target

[Service]

Type=forking

ExecStart=/usr/local/vpnserver/vpnserver start

ExecStop=/usr/local/vpnserver/vpnserver stop

[Install]

WantedBy=multi-user.target

EOF
```
###### OR USE A TEXT EDITOR : ساخت سرویس با تکست ادیتور نانو
```
sudo nano /lib/systemd/system/vpnserver.service
```
###### past the following lines and save the file : اطلاعات زیر رو پیست کنید و فایل رو سیو کنید
```
[Unit]

Description=SoftEther VPN Server

After=network.target

[Service]

Type=forking

ExecStart=/usr/local/vpnserver/vpnserver start

ExecStop=/usr/local/vpnserver/vpnserver stop

[Install]

WantedBy=multi-user.target
```


###### Enable IPv4 & IPv6 Forwarding : فعالسازی آیپی وی 4 و 6
```
echo net.ipv4.ip_forward = 1 | ${SUDO} tee -a /etc/sysctl.conf

echo net.ipv6.ip_forward = 1 | ${SUDO} tee -a /etc/sysctl.conf
```


###### Manage of Server : مدیریت سرور وی پی ان
```
systemctl enable vpnserver

systemctl start vpnserver

systemctl stop vpnserver

systemctl restart vpnserver

systemctl status vpnserver
```

###### Add Ports to Fierwall : قراردادن پورت ها در فایروال
```
sudo ufw allow 500,4500/udp

ufw allow 443

ufw allow 1701

ufw allow 1194

ufw allow 5555
```


###### Download SoftEther: دانلود نرم افزار سافت اتر

```
https://www.softether.org/
```
