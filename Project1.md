## Customising the NGINX Container

### Step1: Pull the image from the docker hub
 - docker pull nginx:1.27.0

Above command pulls the nginx webserver with 1.27.0 tag.

### Step2: Run an Nginx container
- docker run -d -p 80:80 --name my_nginx nginx:1.27.0

If **nginx:1.27.0** is not specified in the above command it considers the latest version.

- docker ps

It list all the availble containers.

### Step3: Access the container's shell
To enter the container interactively, run

- docker exec -it my_nginx bash

This will provide a Bash shell inside the running container.

### Step4: Install vim
Once inside the container, update the package list and install Vim
- apt update && apt install -y vim

### Step5: Modify the index.html File
- vim index.html

Modify the content as needed

- welcome to my_nginx

now we can go to the browser **localhost:80**