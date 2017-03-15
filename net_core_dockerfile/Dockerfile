FROM jetbrains/teamcity-minimal-agent:10.0.5

# Installing https package
RUN apt-get update && \
    apt-get install apt-transport-https -y

# Installing .NET core SDK
RUN sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ xenial main" > /etc/apt/sources.list.d/dotnetdev.list' && \
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893 && \
    apt-get update && \
    apt-get install dotnet-dev-1.0.1 -y