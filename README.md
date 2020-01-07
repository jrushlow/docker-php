# Docker-PHP

Docker environment for developing PHP applications

Keep an eye out for the video demo of the container at [rushlow.dev](https://rushlow.dev)

## WIP
These container are ready for use in development environments, they are not meant 
for production use. Changes are still being made, and the documentation is being
 completed. In the meantime, DO NOT ATTEMPT TO USE THESE CONTAINERS IN PRODUCTION! 

## Getting Started
1) Clone or create a new PHP project on your host. 
Check out [docker-php-workspace container](https://github.com/jrushlow/docker-php-workspace)
and [PHP Workspace Container Video Series](https://rushlow.dev/blog/php-workspace-container-part-1) to create new projects
without the need to have composer, PHP, etc.. installed locally on your host system.

2) Then clone / download this repo into a directory on your host. (Not into the PHP project
you just created.)

3) Copy all of the files within docker-php to a new sub-directory within your newly created PHP project such 
as `project/.docker`.

4) Copy `.docker/.env.DIST` to `.env` and set the appropriate values.

5) Run `.docker/docker-compose build` to build the docker images.

6) Run `.docker/docker-compose up` to start the containers.


## Help / Feedback
As always, any questions, comments, or concerns are always welcome! Check out [rushlow.dev](https://rushlow.dev) for 
contact details or email me directly at `jr@rushlow.dev`.

Jesse Rushlow