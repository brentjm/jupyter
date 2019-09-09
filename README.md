# Docker Jupyter notebook
Jupyter notebook server inside Docker container. The container
is build from pip. The server is run 
conda, but uses tini.

## Overview
* *Dockerfile*
  * Based on Python 3.5-stretch. This can be changed, if desired.
  * Installs python packages using pip3. 
  * Runs Jupyter using tini
* *docker-compose.yml*:
  * Creates the base Jupyter service
  * Opens port 8888
  * defines a bind volume under the current directory
  (./notebook) to store jupyter notebook

## Getting started
1. clone this repository
2. run docker-compose
`$docker-compose up -d`
3. Log into the container and run the following commands
   to enable nbextensions
   `jupyter nbextensions_configurator enable --user`
   `jupyter contrib nbextension install --user`
3. Open browser to localhost:8888

## Customization
1. Save Jupyter notebooks in the bind volume

# Author

**Brent Maranzano**

# License

This project is licensed under the MIT License - see the LICENSE file for details
