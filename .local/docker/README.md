# How to use Docker to develop locally

### Develop

In development we use a combination of Angular Cli to build our front end apps and Nginx to server them. 
We configure Nginx to serve the compiled front end apps via SSL on an app domain (front-end-app.dev.io).

Nginx template for a front end app: 

` .local/nginx/servers/dist/front-end-app.conf`

To map a domain to your localhost you'll need to add the domain to your `/etc/hosts` file:

```bash
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1       localhost
255.255.255.255 broadcasthost
::1             localhost

127.0.0.1       front-end-app.dev.io

```

We use nginx to serve the front end app files from the `/dist`. 
To serve all the apps from the `dist` folder, we can run

```bash
docker-compose -f .local/docker/dev.yml up
```

```bash
ng build front-end-app --aot --source-map --watch
``` 