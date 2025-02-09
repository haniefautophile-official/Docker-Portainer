# Docker-Portainer
``` bash
sudo apt update && sudo apt upgrade -y && sudo apt install nginx -y && sudo apt install php php-fpm php-mysqli -y && sudo apt install mariadb-server mariadb-client -y && sudo apt install phpmyadmin -y && sudo apt install vsftpd -y
```
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```
```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```
echo "deb [arch=arm64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```
echo "deb [arch=arm64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt update
```
```
sudo apt install docker-ce docker-ce-cli containerd.io -y
```
```
sudo docker pull portainer/portainer-ce
```
```
sudo docker volume create portainer_data
```
```
sudo docker run -d -p 9000:9000 -p 9443:9443 --name portainer --restart always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  portainer/portainer-ce
```

Hapus Docker Compose Lama
```
sudo rm -f /usr/local/bin/docker-compose
```
```
sudo rm -f /usr/bin/docker-compose
```
Unduh Versi Terbaru Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-linux-aarch64" -o /usr/local/bin/docker-compose
```
Beri Izin Eksekusi
```
sudo chmod +x /usr/local/bin/docker-compose
```
Cek versi untuk memastikan penginstalan berhasil:
```
docker-compose version
```
<p>Harusnya keluar output seperti:<br>
<p></p>Docker Compose version v2.x.x<br>

<p>Langkah 3: Akses Portainer melalui Web Browser<br>
<p></p>Setelah Portainer dijalankan, Anda dapat mengaksesnya melalui browser di port 9000 (untuk HTTP) atau port 9443 (untuk HTTPS).<br> 
<p>Misalnya, jika alamat IP Armbian Anda adalah 192.168.1.100, buka browser dan akses:</p>

arduino
Salin kode
http://192.168.1.100:9000


<p>Jika anda ingin melanjutkan membuat web maka buat setruktur seperti contoh:</p>
<p>mkdir -p ~/docker/web/minerproperty.my.id<br>
mkdir -p ~/docker/web/haniefautophile.my.id<br>
mkdir -p ~/docker/nginx/conf.d<br>
mkdir -p ~/docker/certbot/www<br>
mkdir -p ~/docker/certbot/conf<br>
mkdir -p ~/docker/dbdata</p>

<p>Ubah folder sesuai yang anda inginkan.</p>
