# Create service


### **The service script:**

```angular2html
[Unit]
Description= Foysal DevOps First HTTP Server

[Service]
ExecStart=python3 -m http.server 7777
WorkingDirectory=/home/ec2-user/younusfoysal
StandardOutput=/home/ec2-user/younusfoysal/server.log
StandardError=/home/ec2-user/younusfoysal/error.log

[Install]
WantedBy=multi-user.target
```


Step 3: Restart the system
```shell
systemctl daemon-reload
```

Step 4: Check status
```shell
systemctl status younusfoysal.service
```

Step 5: Start service
```shell
systemctl start younusfoysal.service
```

Step 6: Reload the service file if any changes
```shell
systemctl daemon-reload
```

Step 7: Restart service
```shell
systemctl restart younusfoysal.service
```

Step 8: To start the service automatically after restarting the server
```shell
systemctl enable younusfoysal.service
```

Step 10: Create an index.html file for publishing under the service
```shell
cd /home/ec2-user/younusfoysal
vi index.html
```

```angular2html
<html>
<title>
</title>
<head>
    <title></title></head>
<body>
    <p> Hello! Foysal!</p>
    <p> Welcome to DevOps Mastering!</p>
</body>
</html>
```

Step 11: Then browse with
```shell
http://18.139.211.175:7777/
```
