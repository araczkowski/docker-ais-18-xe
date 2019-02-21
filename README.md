# RUN an APEX Stack with Docker


## Prerequisites

* clone this repo and go to the folder

    ```bash
    git clone https://github.com/araczkowski/docker-ais-18-xe.git
    cd docker-ais-18-xe
    ```

* Docker pull

    ```bash
    sudo docker pull araczkowski/ais-dom-18-xe
    ```

* Download and unzip your DB files

    ```bash
    sudo tar --same-owner -xvf /tmp/oradata.tar
    ```

## Start the container

Run the script to create and run the container, where the container name is `axer` (it is preferred that you execute a command using `sudo` before executing this script):

    ```bash
    sudo ./03-run.sh ais-dom-xe my.env
    ```

## Use the container
Using the sample settings, the following are accessible:

| Port | Application | URL |
|-|-|-|
| 50080 | APEX | http://localhost:50080 |
| 51521 | Database | N/A |
| 55500 | Enterprise Manager Express | https://localhost:55500/em |


## Moving the container to nex box

    ```bash
    sudo tar -cvpf oradata.tar oradata
    ```

    ```bash
    sudo scp oradata.tar user@host:/tmp
    ```

etc.. 
