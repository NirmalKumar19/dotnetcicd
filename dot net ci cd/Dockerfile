# Stage 1: Build and publish the app
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src

# Copy the project file and restore dependencies
COPY ["dot net ci cd.csproj", "./"]
RUN dotnet restore "dot net ci cd.csproj"

# Copy the rest of the source code
COPY . .

# Publish the application to /out
RUN dotnet publish "dot net ci cd.csproj" -c Release -o /out
