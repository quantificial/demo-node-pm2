# production mode start up
https://www.howtoing.com/install-pm2-to-run-nodejs-apps-on-linux-server

https://www.cnblogs.com/chyingp/p/pm2-documentation.html

https://larrylu.blog/nodejs-pm2-cluster-455ffbd7671


## use pm2 to start node application
pm2 start server.js

## specify the node instance
pm2 start server.js -i 4

## scale the app to n instances
pm2 scale <server_name> <number_of_instance>

## monitor the process
pm2 monit

## show node detail
pm2 show <node_id>

## more commands

$ sudo pm2 stop all                  		#stop all apps
$ sudo pm2 stop 0                    		#stop process with ID 0
$ sudo pm2 restart all               		#restart all apps
$ sudo pm2 reset 0		         	#reset all counters
$ sudo pm2 delete all                		#kill and remove all apps
$ sudo pm2 delete 1                 		#kill and delete app with ID 1


$ sudo pm2 logs                      	#view logs for all processes 
$ sudo pm2 logs 1	         	#view logs for app 1
$ sudo pm2 logs --json               	#view logs for all processes in JSON format
$ sudo pm2 flush			#flush all logs


$ sudo pm2 startup            #enable PM2 to start at system boot
$ sudo pm2 startup systemd    #or explicitly specify systemd as startup system 
$ sudo pm2 save               #save current process list on reboot
$ sudo pm2 unstartup          #disable PM2 from starting at system boot
$ sudo pm2 update	      #update PM2 package

