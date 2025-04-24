# Proyecto MVC MiniCore Notas

## 📌 Descripción
Este proyecto es una aplicación web desarrollada con .NET Core 8 bajo el patrón MVC (Modelo-Vista-Controlador). El objetivo principal es gestionar calificaciones de estudiantes a través de una interfaz sencilla y funcional. La aplicación permite registrar estudiantes, asignar calificaciones y filtrar los datos por fechas específicas.

---

## 📚 Recursos de aprendizaje utilizados

- [Curso de Angular desde cero - YouTube](https://www.youtube.com/watch?v=4dfIDqJbhfY)
- [Documentación oficial de Angular](https://angular.io/docs)
- [Mini tutorial en video explicativo (versión corta)](https://www.loom.com/share/20a22c6e94c7e8787ec04ae5eb7eec9)
- [Video base principal usado para el desarrollo](https://www.youtube.com/watch?v=qf8-JzU-4IE&t=3916s)

---

## 🔗 Enlaces importantes
Repositorio usado: https://github.com/Ivan-Tulcan/IngWeb_Minicore_Notas.git

- 🔗 **Repositorio del Proyecto**: [GitHub - MVCMinicore-Notas](https://github.com/MarioLopez13/MVCMinicore-Notas.git)  
- 🌐 **Deploy del Proyecto**: [Render App - mvcminicore-notas](https://mvcminicore-notas.onrender.com/)  

---

## 🎯 Objetivo
Demostrar que el estudiante posee el conocimiento y habilidades necesarias para la resolución de problemas a través de diferentes herramientas y tecnologías.

---

## 📌 Indicaciones

Este proyecto sigue el patrón MVC con tecnologías modernas. Se recomienda tener conocimientos básicos de C#, .NET, y bases de datos relacionales.  
Es indispensable tener activa la base de datos en Railway para que la aplicación funcione correctamente.

---

## 🔧 Desarrollo

Para esta asignación, se utilizó:

- .NET Core 8
- MySQL (conectado mediante Railway)
- Arquitectura MVC

### 📂 Estructura del modelo:

- **Estudiante**: Clase con propiedades `Id` y `Nombre`, utilizada para identificar al alumno.
- **Calificación**: Clase con propiedades `Id`, `Fecha`, `Nombre` (nombre de la actividad/calificación), y `EstudianteId` (llave foránea).

---

## 🛠️ Instrucciones de uso

1. Clona el repositorio:
   ```bash
   git clone https://github.com/MarioLopez13/MVCMinicore-Notas.git
