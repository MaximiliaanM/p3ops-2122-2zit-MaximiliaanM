
# asp.net SDK versie 5.0
FROM mcr.microsoft.com/dotnet/aspnet:5.0 As base
WORKDIR /app
EXPOSE 80
ENV ASPNETCORE_URLS=http://+:80

# Copy csproj and restore as distinct layers
FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /
COPY ./SportStore.sln ./
COPY ./src/Domain/Domain.csproj ./src/Domain/
COPY ./src/Services/Services.csproj ./src/Services/

COPY ./src/Server/Server.csproj ./src/Server/
COPY ./src/Shared/Shared.csproj ./src/Shared/
COPY ./src/Client/Client.csproj ./src/Client/
RUN dotnet restore

# Copy everything else and build app
COPY ./ ./
COPY ./src/Domain/ ./src/Domain/
COPY ./src/Services/ ./src/Services/
COPY ./src/Server/ ./src/Server/
COPY ./src/Shared/ ./src/Shared/
COPY ./src/Client/ ./src/Client/


WORKDIR /src/Domain
RUN dotnet build -c Release -o /app/out
WORKDIR /src/Services
RUN dotnet build -c Release -o /app/out
WORKDIR /src/Server
RUN dotnet build -c Release -o /app/out
WORKDIR /src/Shared
RUN dotnet build -c Release -o /app/out
WORKDIR /src/Client
RUN dotnet build -c Release -o /app/out
WORKDIR /
RUN dotnet build -c Release -o /app/out

FROM build AS publish
RUN dotnet publish -c Release -o /app/out

# Build runtime image
FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS runtime
WORKDIR /app
COPY --from=publish /app/out .
ENTRYPOINT ["dotnet", "Server.dll"]