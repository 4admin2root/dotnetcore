# install on centos
https://www.microsoft.com/net/core#linuxcentos
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[packages-microsoft-com-prod]\nname=packages-microsoft-com-prod \nbaseurl=https://packages.microsoft.com/yumrepos/microsoft-rhel7.3-prod\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/dotnetdev.repo'
sudo yum update
sudo yum install libunwind libicu
sudo yum install dotnet-sdk-2.0.0
```

# boot from docker
```
docker run -it microsoft/dotnet:latest
```

# demo
1
```
dotnet new console -o hwapp
cd hwapp
dotnet run
```
2
```
dotnet new web -o website
cd website
export ASPNETCORE_URLS='http://*:5000'
dotnet run
```
or

```
dotnet new web -o website
cd website
export ASPNETCORE_URLS='http://*:5000'
dotnet build -o app
dotnet app/website.dll
```
