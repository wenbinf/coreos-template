# CoreOS template for dev and prod

Each repo (source code) of my project will have a subdirectory deploy/, including contents of this coreos-template repo.

The basic idea for this setup:
* Docker Hub builds images.
* units/ includes fleet unit files to start services (docker containers), pulling from Docker Hub. These unit files are used by both dev and prod.
* dev/ is to start a vagrant box for dev environment. (TODO: add script to concatenate unit files into user-data)
* prod/ includes cloud-config for prod environment. (TODO: add script to concatenate unit files into cloud-config)
