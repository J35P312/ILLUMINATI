Bootstrap: docker
From: ubuntu:16.04

%environment
SHELL=/bin/bash
LC_ALL=C.UTF-8


%runscript
    echo "This is what happens when you run the container..."

%post
    echo "Hello from inside the container"
    apt-get update
    apt-get -y install wget git bzip2 build-essential gcc zlib1g-dev language-pack-en-base apt-transport-https make cmake unzip libncurses5-dev libncursesw5-dev
    update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8

    wget -q https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb
    dpkg -i packages-microsoft-prod.deb

    apt-get update
    apt-get -y install dotnet-sdk-2.1
         

    sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893

    apt-get update
    apt-get -y install dotnet-dev-1.0.4

    mkdir /Nirvana
    cd /Nirvana/ && wget https://github.com/Illumina/Nirvana/releases/download/v2.0.9/2.0.9.zip
    unzip /Nirvana/2.0.9.zip

    mkdir /Canvas
    cd /Canvas && wget https://github.com/Illumina/canvas/releases/download/1.35.1.1316%2Bmaster/Canvas-1.35.1.1316.master_x64.tar.gz
    tar -xvf /Canvas/Canvas-1.35.1.1316.master_x64.tar.gz
    mv /Canvas/Canvas-1.35.1.1316+master_x64/* /Canvas/
