FROM jetbrains/teamcity-minimal-agent:10.0.5

# Installing somepackages (https npm and some bower and gulp for npm)
RUN apt-get update && \
    apt-get install apt-transport-https -y && \
    apt-get install npm -y && \
    npm install npm -g && \
    npm install bower gulp -g

# Installing .NET core SDK
RUN sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ yakkety main" > /etc/apt/sources.list.d/dotnetdev.list' && \
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893 && \
    apt-get update && \
    apt-get install dotnet-dev-1.0.1