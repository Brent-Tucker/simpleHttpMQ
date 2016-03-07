# simpleHttpMQ

## Requirements:

1.OpenResty has been installed under /usr/local/openresty, please refer to http://www.openresty.org/ for details.

2.Redis has been installed and without authentication settings.

## Usage:

1. Modify the redis settings in lua/appConfig.lua, the defaults are localhost and 6379.

2. Start the app by running the shell file ./startup.sh, please modify the execution permission if it can't start.

3. Access the url *http://localhost:6699/httpmq/sendMessage?queueName=queue1&message=msg123* to send a message, and access the url *http://localhost:6699/httpmq/getMessage?queueName=queue1* to retrieve messages.

4. In your applications, you can use above URLs to send and retrieve messages, the key URL parameters are "queueName" and "message".


