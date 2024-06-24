# PyPamProcessAgent

A PyPam Testing Repository


# Overview

This project was created as part of a larger effort to process acoustic data at scale. The pypam library is a technology implemented in the form of a python package which processes hydrophone data and this project was created to wrap pypam processes into a highly deployable forms which grant configurability, automation  horizontal scaling. The interpretation is that a docker run command would spawn a a process job and would run until an entire hydrophone deployment is processed.

# Workflow

To process a deployment with pypam by operating on a hydrophone-generated-wavefile-directory.



- Run command:

        $ docker run pypam-process-agent -it 
        -e "external_deployment_path = <external_deployment_path>"
        -e "external_output_path = <external_output_path>" 
        -e "model = <model>" 
        -e "serial_number = <serial_number>" 
        -e "port = <port_number>"

- Example command:

        $ docker run pypam-process-agent -it 
        -e "external_deployment_path = /home/user/Documents/deployment" 
        -e "external_output_path = /home/user/Documents/pypam_output" 
        -e "model = STH600" 
        -e "serial_number = XXXXXXX" 
        -e "port = 8000"


If you wish to build from the Dockerfile:

- Build Command:

        $ docker build -it pypam-process-agent .

