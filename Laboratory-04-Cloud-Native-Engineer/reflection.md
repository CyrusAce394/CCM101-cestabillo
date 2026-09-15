# Mission Reflection

This activity helped me understand the use of containerization in cloud computing and also the differences between containerization and the use of VMs. Containers are quicker to install than an installation of an OS on a VM because containers do not have to install a complete guest operating system. As part of the activity, I was able to download an Nginx image and run the web server within one minute. It helped me to see that containers are more efficient in application deployment than virtual machines.

Also, as part of this task, I understood the importance of port mapping when running a web server on a container. With the help of the `-p 8080:80` argument, port 8080 on the host machine is mapped to port 80 of the container, also giving me access to the Nginx web server from the host. Understanding the container lifecycle management also helped me learn how to list, stop, and remove containers through docker commands. While removing the container through the `docker rm` command, the container is entirely deleted, so all the important data should be stored anywhare if they are necessary.

Containerization could also facilitate cooperation between software developers and IT operations teams since applications can be packed with dependencies and then be deployed in the same way. With this, containerization can support the principles of DevOps through promoting collaboration.

As i learned on this activity, this activity helped me to add a new cloud computing lab to my GitHub portfolio. It also helped me gain practical skills working with Docker, Nginx, containers management, and technical documentation.
