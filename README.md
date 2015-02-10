# self-signed-wildcard-cert


Generating of self signed wildcard certificates using openssl. Certificates were used under IIS 7.

I use for my local sites domain "local" and 127.0.0.1 for all bindings.

- timesheet.local
- graph.local
- etc

And for developer server my sites also have one IP-address and names:

- timesheet.devserver
- graph.devserver
- etc

So in my black and grey area I use only one IP-address like it is on my live server. I want to have one self signed sertificate for whole server. 

For simple generating of certificates for both servers I created script ```go-cert```. All I need is:

- add into to directory of script config file with name ```wildcard.YOUR_DOMAIN.cnf```
- specify DNS-names and IP-addresses in [alt_names] section
- call ```$ ./go-cert YOUR_DOMAIN```

Useful links:

- [https://www.openssl.org/docs/apps/req.html](https://www.openssl.org/docs/apps/req.html)
- [http://andyarismendi.blogspot.ru/2011/09/creating-certificates-with-sans-using.html](http://andyarismendi.blogspot.ru/2011/09/creating-certificates-with-sans-using.html)
- [https://www.madboa.com/geek/openssl/](https://www.madboa.com/geek/openssl/)