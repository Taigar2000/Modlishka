你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# ..Modlishka..

Modlishka is a flexible and powerful reverse proxy, that will take your phishing campaigns to the next level (with minimal effort required from your side). 
 
Enjoy :-)


Features
--------

Some of the most important 'Modlishka' features :

-   Support for majority of 2FA authentication schemes (by design).
-   No website templates (just point Modlishka to the target domain - in most cases, it will be handled automatically).
-   Full control of "cross" origin TLS traffic flow from your victims browsers.
-   Flexible  and easily configurable phishing scenarios through configuration options.
-   Pattern based JavaScript payload injection.
-   Striping website from all encryption and security headers (back to 90's MITM style). 
-   User credential harvesting (with context based on URL parameter passed identifiers).
-   Can be extended with your ideas through plugins.
-   Stateless design. Can be scaled up easily for an arbitrary number of users - ex. through a DNS load balancer.
-   Web panel with a summary of collected credentials and user session impersonation (beta).
-   Written in Go.


Action
------
_"A picture is worth a thousand words":_

 Modlishka in action against an example 2FA (SMS) enabled authentication scheme:

[![Watch the video](https://i.vimeocdn.com/video/749353683.jpg)](https://vimeo.com/308709275)

[https://vimeo.com/308709275](https://vimeo.com/308709275)

Note: google.com was chosen here just as a POC.


Installation
------------

Latest source code version can be fetched from [here](https://github.com/drk1wi/modlishka/zipball/master) (zip) or [here](https://github.com/drk1wi/modlishka/tarball/master) (tar).

Fetch the code with _'go get'_ :

    $ go get -u github.com/drk1wi/Modlishka

Compile the binary and you are ready to go:

    $ cd $GOPATH/src/github.com/drk1wi/Modlishka/
    $ make
    
    
![alt text](https://raw.githubusercontent.com/drk1wi/assets/master/7d0426a133a85a46a76a424574bf5a2acf99815e.png)

    # ./dist/proxy -h
  
    
    Usage of ./dist/proxy:
          
      -cert string
        	base64 encoded TLS certificate
      
      -certKey string
        	base64 encoded TLS certificate key
      
      -certPool string
        	base64 encoded Certification Authority certificate
      
      -config string
        	JSON configuration file. Convenient instead of using command line switches.
      
      -credParams string
          	Credential regexp collector with matching groups. Example: base64(username_regex),base64(password_regex)

      -debug
        	Print debug information
      
      -disableSecurity
        	Disable security features like anti-SSRF. Disable at your own risk.
      
      -jsRules string
        	Comma separated list of URL patterns and JS base64 encoded payloads that will be injected. 
      
      -listeningAddress string
        	Listening address (default "127.0.0.1")
      
      -listeningPort string
        	Listening port (default "443")
      
      -log string
        	Local file to which fetched requests will be written (appended)
      
      -phishing string
        	Phishing domain to create - Ex.: target.co
      
      -plugins string
        	Comma seperated list of enabled plugin names (default "all")
      
      -postOnly
        	Log only HTTP POST requests
      
      -rules string
        	Comma separated list of 'string' patterns and their replacements. 
      
      -target string
        	Main target to proxy - Ex.: https://target.com
      
      -targetRes string
        	Comma separated list of target subdomains that need to pass through the  proxy 
      
      -terminateTriggers string
        	Comma separated list of URLs from target's origin which will trigger session termination
      
      -terminateUrl string
        	URL to redirect the client after session termination triggers
      
      -tls
        	Enable TLS (default false)
      
      -trackingCookie string
        	Name of the HTTP cookie used to track the victim (default "id")
      
      -trackingParam string
        	Name of the HTTP parameter used to track the victim (default "id")




Usage
-----

 * Check out the [wiki](https://github.com/drk1wi/Modlishka/wiki) page for a more detailed overview of the tool usage.
 * [FAQ](https://github.com/drk1wi/Modlishka/wiki/FAQ) (Frequently Asked Questions)
 * [Blog post](https://blog.duszynski.eu/phishing-ng-bypassing-2fa-with-modlishka/)


License
-------
Modlishka was made by Piotr Duszyński ([@drk1wi](https://twitter.com/drk1wi)). You can find the license [here](https://github.com/drk1wi/Modlishka/blob/master/LICENSE).

Credits
-------
Thanks for helping with the code go to Giuseppe Trotta ([@Giutro](https://twitter.com/giutro)) 


Disclaimer
----------
This tool is made only for educational purposes and can be only used in legitimate penetration tests. Author does not take any responsibility for any actions taken by its users.

-------

[![Twitter](https://img.shields.io/badge/twitter-drk1wi-blue.svg)](https://twitter.com/drk1wi)


