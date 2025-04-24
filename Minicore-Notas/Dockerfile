FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["Minicore-Notas/Minicore-Notas.csproj", "Minicore-Notas/"]
WORKDIR /src/Minicore-Notas
RUN dotnet restore "Minicore-Notas.csproj"
COPY . .
RUN dotnet publish "Minicore-Notas.csproj" -c Release -o /app/out

FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "Minicore-Notas.dll"]
