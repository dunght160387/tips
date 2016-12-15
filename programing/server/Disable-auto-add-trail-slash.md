Disable auto add trail to slash
===============================
For apache2, add this config to your site config (/etc/apache2/sites-availabel/your-site.conf

```
<Location /log>
	# disable add trailing slash. e.g: log?type=... instead of log/?type=...
	DirectorySlash Off
	#SetHandler some-handler
</Location>
```

then reload apache2

```
sudo service apache2 reload
```
