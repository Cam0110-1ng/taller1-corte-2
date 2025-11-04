# Guía de Inicio Rápido

## 👋 Bienvenido

Esta guía te ayudará a comenzar con el proyecto **Taller 1 - Corte 2** de manera rápida y efectiva.

## 🎯 ¿Qué es este Proyecto?

Este es un proyecto académico que forma parte del segundo corte de un curso. Su objetivo es aplicar conocimientos de programación y desarrollo de software en un proyecto práctico.

## 📦 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

### 1. Git
```bash
# Verificar si Git está instalado
git --version

# Si no está instalado, descargarlo de:
# https://git-scm.com/downloads
```

### 2. Cuenta de GitHub
- Crea una cuenta en [GitHub](https://github.com) si no tienes una
- Configura tu usuario de Git:
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@ejemplo.com"
```

### 3. Editor de Código
Recomendaciones:
- [Visual Studio Code](https://code.visualstudio.com/) (Recomendado)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/)
- [Sublime Text](https://www.sublimetext.com/)

## 🚀 Configuración Inicial

### Paso 1: Clonar el Repositorio

```bash
# Opción 1: HTTPS
git clone https://github.com/Cam0110-1ng/taller1-corte-2.git

# Opción 2: SSH (si tienes configurada tu llave SSH)
git clone git@github.com:Cam0110-1ng/taller1-corte-2.git

# Entrar al directorio del proyecto
cd taller1-corte-2
```

### Paso 2: Explorar la Estructura

```bash
# Ver los archivos del proyecto
ls -la

# Ver el contenido del README
cat README.md

# Abrir el proyecto en VS Code
code .
```

### Paso 3: Verificar el Estado

```bash
# Ver el estado actual de Git
git status

# Ver las ramas disponibles
git branch -a

# Ver el historial de commits
git log --oneline
```

## 📝 Flujo de Trabajo Básico

### 1. Crear una Nueva Rama

```bash
# Crear y cambiar a una nueva rama
git checkout -b feature/mi-nueva-funcionalidad

# Verificar que estás en la rama correcta
git branch
```

### 2. Hacer Cambios

- Abre los archivos en tu editor
- Realiza las modificaciones necesarias
- Guarda los cambios

### 3. Ver los Cambios

```bash
# Ver qué archivos han cambiado
git status

# Ver los cambios específicos
git diff
```

### 4. Preparar los Cambios (Stage)

```bash
# Agregar un archivo específico
git add nombre_archivo.ext

# Agregar todos los archivos modificados
git add .

# Ver qué está preparado para commit
git status
```

### 5. Hacer Commit

```bash
# Hacer commit con un mensaje descriptivo
git commit -m "Descripción clara del cambio realizado"

# Ejemplo de buen mensaje de commit:
git commit -m "Agregar función de validación de datos"
```

### 6. Sincronizar con GitHub

```bash
# Subir los cambios al repositorio remoto
git push origin feature/mi-nueva-funcionalidad

# Si es la primera vez que subes esta rama:
git push -u origin feature/mi-nueva-funcionalidad
```

## 🔄 Comandos Git Útiles

### Ver Información

```bash
# Ver el estado actual
git status

# Ver el historial de commits
git log

# Ver el historial de manera compacta
git log --oneline --graph --all

# Ver cambios no preparados
git diff

# Ver cambios preparados
git diff --staged
```

### Gestionar Cambios

```bash
# Descartar cambios en un archivo
git checkout -- nombre_archivo.ext

# Descartar todos los cambios no preparados
git checkout -- .

# Quitar un archivo del área de preparación
git reset nombre_archivo.ext

# Ver ramas
git branch

# Cambiar de rama
git checkout nombre_rama

# Crear y cambiar a una nueva rama
git checkout -b nombre_nueva_rama
```

### Sincronizar

```bash
# Descargar cambios del repositorio remoto
git fetch

# Descargar e integrar cambios
git pull

# Subir cambios
git push
```

## 📚 Convenciones y Buenas Prácticas

### Nombres de Ramas

```
feature/nombre-funcionalidad    # Para nuevas características
bugfix/nombre-bug               # Para corrección de errores
hotfix/nombre-hotfix            # Para correcciones urgentes
docs/nombre-documentacion       # Para documentación
```

### Mensajes de Commit

✅ Buenos ejemplos:
```
"Agregar validación de formulario de login"
"Corregir error en cálculo de totales"
"Actualizar documentación de API"
"Refactorizar función de búsqueda"
```

❌ Malos ejemplos:
```
"cambios"
"update"
"fix"
"asdf"
```

### Estructura de Archivos

```
taller1-corte-2/
├── README.md              # Siempre actualizar con cambios importantes
├── src/                   # Código fuente aquí
├── tests/                 # Pruebas aquí
├── docs/                  # Documentación adicional
└── .gitignore            # Archivos a ignorar por Git
```

## 🐛 Solución de Problemas Comunes

### Problema: "Permission denied (publickey)"

**Solución**: Necesitas configurar tu llave SSH
```bash
# Generar una nueva llave SSH
ssh-keygen -t ed25519 -C "tu_email@ejemplo.com"

# Agregar la llave al ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Copiar la llave pública y agregarla en GitHub
cat ~/.ssh/id_ed25519.pub
```

### Problema: "fatal: not a git repository"

**Solución**: No estás en el directorio correcto
```bash
# Navegar al directorio del proyecto
cd /ruta/al/proyecto/taller1-corte-2
```

### Problema: Conflictos al hacer pull

**Solución**: 
```bash
# Opción 1: Guardar tus cambios temporalmente
git stash
git pull
git stash pop

# Opción 2: Hacer commit primero
git add .
git commit -m "Guardar cambios locales"
git pull
```

### Problema: Olvidé en qué rama estoy

**Solución**:
```bash
# Ver la rama actual
git branch

# La rama con * es la actual
# También se puede ver con:
git status
```

## 🎓 Próximos Pasos

1. **Familiarízate con el código**: Lee los archivos existentes
2. **Entiende los requisitos**: Revisa las especificaciones del taller
3. **Planifica tu trabajo**: Antes de codificar, piensa en la solución
4. **Desarrolla incrementalmente**: Haz pequeños cambios y pruébalos
5. **Documenta tu trabajo**: Actualiza el README y agrega comentarios
6. **Haz commits frecuentes**: No esperes a tener todo listo

## 📖 Recursos de Aprendizaje

### Git y GitHub
- [Git - La Guía Sencilla](http://rogerdudler.github.io/git-guide/index.es.html)
- [GitHub Docs en Español](https://docs.github.com/es)
- [Learn Git Branching](https://learngitbranching.js.org/?locale=es_ES)

### Markdown (para documentación)
- [Guía de Markdown](https://www.markdownguide.org/basic-syntax/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)

### Programación
- Documentación oficial del lenguaje que uses
- [Stack Overflow](https://stackoverflow.com/) para preguntas
- [MDN Web Docs](https://developer.mozilla.org/es/) (para web)

## 💡 Consejos Finales

1. **Haz commits frecuentes**: Es mejor hacer muchos commits pequeños que pocos grandes
2. **Escribe mensajes claros**: Tu yo del futuro te lo agradecerá
3. **Lee la documentación**: Antes de preguntar, revisa los docs
4. **Practica**: La única forma de mejorar es practicando
5. **No tengas miedo de experimentar**: Siempre puedes deshacer cambios con Git
6. **Pide ayuda cuando la necesites**: Todos empezamos sin saber

## 🆘 ¿Necesitas Ayuda?

Si tienes problemas:

1. Revisa esta guía nuevamente
2. Consulta la documentación de Git
3. Busca el error en Google o Stack Overflow
4. Pregunta al instructor o compañeros
5. Crea un issue en GitHub con tu pregunta

---

¡Buena suerte con tu taller! 🚀

**Última actualización**: Noviembre 2025