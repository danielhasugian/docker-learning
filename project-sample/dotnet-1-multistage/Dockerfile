FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build-env
WORKDIR /app
COPY src .
RUN dotnet publish -c Release -o out

FROM mcr.microsoft.com/dotnet/aspnet
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80
WORKDIR /app
COPY --from=build-env /app/out ./
ENTRYPOINT ["dotnet", "src.dll"]