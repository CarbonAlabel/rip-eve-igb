# rip-eve-igb
Gently tell the visitors of your website that they shouldn't be using the EVE Online in-game browser anymore.

This nginx config snippet will ensure that all visitors to your site get a reminder that they really shouldn't be using the IGB.

## Instructions
Move the [no_igb.html](no_igb.html) file to `/usr/share/nginx` and the [no_igb.conf](no_igb.conf) file to `/etc/nginx`.
Include the configuration file in your server block. Example:
````nginx
server{
	server_name example.com;
	listen 443 ssl http2;
	listen [::]:443 ssl http2;
	root /usr/share/nginx/example;
	
	#Rest of your configuration goes here...
	
	include /etc/nginx/no_igb.conf;
}
````
