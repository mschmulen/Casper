##Driskill ghost theme

A theme for the Ghost Blogging platform - forked from Casper, the default [Ghost](http://ghost.org) theme.

The Driskill Hotel in Austin, Texas is the most haunted building hotel in Texas, perhaps the U.S.

###How to install the Driskill ghost theme

1. Login to your machine.

```
cd /var/www/ghost/content/themes/
```

2. Make sure your up to date and you have git installed

```
apt-get update
apt-get install git-core -y
```

3. Clone your repo from a public git, and update the owner of the files to ghost user and group

```
git clone https://github.com/mschmulen/Driskill
chown -R ghost:ghost Driskill
```

4. Restart your ghost service

```
service ghost restart
```

5. Just go to your Ghost panel and change your theme 

	[your_domain_name/ghost/settings/general](http://your_domain_name/ghost/settings/general)
	
	[your_domain_name/ghost/settings](http://your_domain_name/ghost/settings)





####Adding Google Analytics to the theme

Insert the following google analytics snippet before the ``` </head> ``` default.hbs 

```
	<script>
	  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
	
	  ga('create', 'UA-99999999-9', 'myDomain.com');
	  ga('send', 'pageview');
	
	</script>

```


