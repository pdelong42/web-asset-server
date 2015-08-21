I figured it was better to explain my motivations in a README file,
than to trickle it out piecemeal in overly verbose commit messages.
    
These are changes I've made to allow for the possibility of fronting
the web-asset-server with a proxy or alternate web server (e.g.,
Apache's mod_proxy).

I need to run the web-asset-server on a non-privileged port, since I
don't want to run it as root.  But I also want it to be accessible to
the public Internet, and local firewall policy in my organization
doesn't allow public access to non-standard ports.

Since this will probably be public-facing, I'd like to possibly wrap
SSL around it in the near future (so, that's another reason for
wanting to front it with a proxy).  But it might be a moot point,
since I don't even know if the Specify client software supports
talking to an asset server over HTTPS.

There's probably a better way to do what I'm doing (probably involving
CGI variables), so feel free to scrap my code in favor of doing it the
right way. :-)
