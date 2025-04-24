FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build

WORKDIR /src

# Copia solo el .csproj para restaurar dependencias primero (más cacheable)
COPY ["Minicore-Notas/Minicore-Notas.csproj", "Minicore-Notas/"]

# Establece el directorio de trabajo dentro del proyecto
WORKDIR /src/Minicore-Notas

# Restaura paquetes NuGet
RUN dotnet restore "Minicore-Notas.csproj"

# Copia el resto de los archivos del proyecto
COPY . .

# Limpia carpetas temporales para evitar errores de acceso
RUN rm -rf bin/ obj/

# Publica la app en modo Release en una carpeta fuera de bin/ para evitar conflictos
RUN dotnet publish "Minicore-Notas.csproj" -c Release -o /app/out

# Imagen de runtime
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime

WORKDIR /app

# Copia los archivos publicados desde la fase de build
COPY --from=build /app/out .

# Define el punto de entrada de la app
ENTRYPOINT ["dotnet", "Minicore-Notas.dll"]

