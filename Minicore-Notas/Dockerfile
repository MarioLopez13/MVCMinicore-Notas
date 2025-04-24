# Etapa de compilación
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build

# Establece un directorio de trabajo neutral fuera del árbol del código fuente
WORKDIR /app

# Copia solo el archivo .csproj para restaurar dependencias primero
COPY Minicore-Notas/Minicore-Notas.csproj ./Minicore-Notas/

# Restaura paquetes NuGet
RUN dotnet restore ./Minicore-Notas/Minicore-Notas.csproj

# Copia el resto del código fuente
COPY Minicore-Notas/ ./Minicore-Notas/

# Publica en una carpeta aislada para evitar problemas de acceso
RUN dotnet publish ./Minicore-Notas/Minicore-Notas.csproj -c Release -o /out --no-restore

# Etapa de runtime
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime

WORKDIR /app

# Copia los archivos publicados
COPY --from=build /out .

# Define el punto de entrada
ENTRYPOINT ["dotnet", "Minicore-Notas.dll"]
