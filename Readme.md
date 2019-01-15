# About

Alpine linux xfce4 rdp server

# Usage

I use this for building a small desktop image with the openshift cli included and to provide easy and secure access to the openshift webconsole

thanks to https://github.com/saily/openshift-cli  for the code to get the okd / openshift command line tools working on alpine

build:

in directory with Dockerfile run: 

```bash
	docker build -t <yourimagename> . 
```

Start the server
```bash
	docker run -d --shm-size 1g --name rdp -p 3389:3389 <yourimagename>
```

*note --shm-size 1g is for firefox, without it it crashes

Connect with your favorite rdp client or use http://guacamole.apache.org/ for more secure access via a browser and html5. works great

User: alpine
Pass: alpine
