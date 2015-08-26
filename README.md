# Nginx-Marathon-Bridge
This is a simple script to generate the configuration files for each Marathon App individully.

Install:

download the Git repo

git clone https://github.com/rajivreddy/Nginx-Marathon-Bridge.git

cd Nginx-Marathon-Bridge/

Process to Run:

Install the Nginx

create a "temp.d" directory in /etc/nginx/

mkdir -p /etc/nginx/temp.d

Update the nginx config file: 

vim /etc/nginx/nginx.conf
add this line in HTTP block
http {
---
---
---
include /etc/nginx/test.d/*.conf;
}


it has only 1 input paramater, i.e, Marathon Link.

run as ./Nginx-Marathon-Bridge URLof Marathon(example.com:8080)

Checking:

Once you ran the above command, check weathe files are created or not

ls /etc/nginx/temp.d/

if it's created the files then Process successfully

You can access the application using 

IP of your server:service_port of Marathon App
Ex:

192.168.0.10:10002

Here 192.168.0.10 is your server IP and 10002 is service port of Marathon App.
