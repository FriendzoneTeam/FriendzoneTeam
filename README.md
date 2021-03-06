![alt tag](https://k60.kn3.net/E/7/C/E/6/0/331.jpg)
# FriendzoneTeam

# SocialServer with Go

Application that lets you run commands on the server (Ubuntu / Debian) via twitter. (developed golang)

# Prerequisites
* A deb based linux distribution
* openssh
* go 1.5+

# Installation
Edit the file: services/services.go and change lines: 25, 26 and 27
Add your Twitter Api

    anaconda.SetConsumerKey("")
    anaconda.SetConsumerSecret("")
    api := anaconda.NewTwitterApi("", "")

And add your ssh configuration (recommended root for servers use) at line 97 and 135

    out, err := ssh.Conekta("USER", "PASS", "HOST", comando.Command)
    
# Examples
(Desfault directory is $HOME/ for all examples)
Send a DM to your twitter Account
* Create a file: Without spaces, third parameter optional (Desfault is $HOME/)
  * create hello.go $GOPATH/src/hello
  * create error_log
* Create a Directory: Without spaces and "/" at the end (Desfault directory is $HOME/)
    * create backups/
    * create logs/ /var/www
    * create user/ /home/
* Delete a file: only filename (Desfault directory is $HOME/)
    * delete error_log
    * delete $GOPATH/src/hello/hello.go
* Delete a Directory: complete route and "/" at the end (Desfault directory is $HOME/)
    * delete $GOPATH/src/hello/
    * delete work/src/hello/
* Move a File (Desfault directory is $HOME/)
    * move error_log $HOME/Backups/
    * move error_log Backups
* Move a Directory
    * move logs/ /var/www
    * move logs/ $HOME/Backups/
* Rename a file
    * rename error_log error_log.1
* Rename a Directory
    * move logs/ error_logs/
    * move logs/ acces_logs
* Create, Start, Restart and Stop servers
    * Create a Go Server: 
        * server new go
    * Create a Lemp (Linux, Nginx, MySQL, PHP) Server:
        * server new lemp
    * Create a Lamp (Linux, Apache, MySQL, PHP) Server:
        * server new lamp
    * Create a Mean (MongoDB, Express, Angular, NodeJS)
        * server new mean
    * Start a Service
        * server start mysql
    * Restart a Service
        * server restart nginx
    * Stop a Service
        * server stop tor
* Execute a bash command:include ":" at the start
    * :shutdown -h +60
* Execute a personalized command
    * Send a DM to your Twitter Account with ":" at first
    ![alt tag](https://k60.kn3.net/F/9/5/B/7/5/5FD.png)
* Restart Apache2 Server && Install new Server go
    ![alt tag](https://k60.kn3.net/5/6/3/F/D/8/A61.png)

# Features
* Anaconda
* Gorilla
* uper.iot
* gonfig

# Team
* Arizpe Paul, @[kiramishima](https://twitter.com/kiramishima), [Github](https://github.com/kiramishima)
* Fabela Wendy, @[Ritalin_P](https://twitter.com/ritalin_p)
* Sierra Jorge, @[Chemasmas](https://twitter.com/chemasmas)
* Osorio Ricardo, [rk521@hotmail.com](mailto:rk521@hotmail.com)

# Bugs
* Use root account in ssh configuration to create a new server (this is not recommended)
* [Warning] DM's must be deleted manually as running
