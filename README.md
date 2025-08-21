# Proyecto en Equipo - Clase de Git & GitHub

Este es un proyecto **colaborativo** para practicar el uso de Git y GitHub en equipo.  

---

## 🚀 Objetivo
- Aprender a trabajar con **ramas (branches)**.  
- Practicar **pull requests** y revisiones de código.  
- Colaborar en equipo como en un proyecto real.  

---

## 📌 Tareas sugeridas
- [ ] Agregar un párrafo en `index.html`.  
- [ ] Crear un botón en `index.html`.  
- [ ] Modificar estilos en `style.css`.  
- [ ] Crear una nueva sección en la página.  

---

## 💻 Comandos de Git que usaremos

### 🔧 Configuración inicial
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
git --version
git config --list

📂 Crear y movernos entre repositorios
git init                   # Inicia un repositorio local
git clone <url-del-repo>   # Clona un repositorio existente

📌 Estados y commits
git status                 # Ver el estado de los archivos
git add .                  # Agregar todos los cambios al área de preparación
git add archivo.txt        # Agregar un archivo específico
git commit -m "Mensaje"    # Guardar cambios en el historial
git log --oneline          # Ver historial de commits resumido

🌿 Ramas
git branch                 # Ver todas las ramas
git checkout -b nueva-rama # Crear y movernos a una nueva rama
git checkout main          # Cambiar a otra rama (ej: main)

⬆️ Subir y bajar cambios
git remote add origin <url> # Conectar repositorio local con GitHub
git push -u origin main     # Subir cambios a la rama main
git push origin rama        # Subir una rama al remoto
git pull                    # Traer los cambios más recientes

🔄 Colaboración

Crear una rama → git checkout -b feature-nueva

Hacer cambios → git add . + git commit -m "mensaje"

Subir la rama → git push origin feature-nueva

Crear un Pull Request en GitHub para que el líder lo revise.

🔙 Volver a un commit (sin borrar historial)
git checkout <id-del-commit> #👉 Se usa cuando quieres regresar a un estado anterior pero sin perder lo que vino después.
git checkout -b volver-al-pasado # Si quieres trabajar desde ahí, lo recomendable es crear una rama

🔄 Establecer un commit como el principal (reescribir historial)
git reset --hard <id-del-commit> #git reset (mueve la rama a un commit anterior)
# ⚠️ Borra todo lo que vino después en esa rama (se pierde el historial posterior).

Si no quieres borrar los archivos, solo mover la rama:
git reset --soft <id-del-commit>

git revert (más seguro en equipo): 
git revert <id-del-commit> #En lugar de borrar commits, crea un nuevo commit que deshace los cambios:

🧠 Resumen rápido:

# Volver a un commit sin afectar nada:
git checkout <commit>
# Dejar ese commit como el último (reescribir historia):
git reset --hard <commit>
# Deshacer cambios de un commit pero sin borrar historia:
git revert <commit>



# -------------------------------------------------------

⚙️ Método alternativo (configuración manual en JSON)

Si no te aparece Git Bash en la lista, haz esto:

Abre la paleta de comandos (Ctrl + Shift + P) y escribe:
"Preferences: Open User Settings (JSON)".

Agrega esta configuración dentro del archivo:
{
  "terminal.integrated.profiles": {
    "Git Bash": {
      "path": "C:\\Program Files\\Git\\bin\\bash.exe"
    }
  },
  "terminal.integrated.defaultProfile.windows": "Git Bash"
}


Guarda el archivo y reinicia VS Code.

Ahora cada vez que abras la terminal, arrancará con Git Bash.