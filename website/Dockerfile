FROM microsoft/dotnet:2.0-sdk
WORKDIR /app
ENV ASPNETCORE_URLS http://*:5000
EXPOSE 5000
COPY app/* /app/
ENTRYPOINT ["dotnet","website.dll"]
