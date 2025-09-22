🌱 1. Crear una nueva rama

Desde tu terminal, dentro del proyecto:

git checkout -b nombre-de-tu-rama


Ejemplo:

git checkout -b feature-login


🔹 Esto hace dos cosas a la vez:
1️⃣ Crea la rama feature-login.
2️⃣ Te mueve automáticamente a esa rama.

💾 2. Hacer cambios y guardarlos

Edita archivos, agrega código, etc.
Luego guarda los cambios en git:

git add .
git commit -m "Agrego pantalla de login"

☁️ 3. Subir la nueva rama a GitHub

La primera vez que subes una rama, usa:

git push -u origin nombre-de-tu-rama


Ejemplo:

git push -u origin feature-login


🔹 El -u guarda la relación para que en el futuro solo necesites git push.

🔄 4. Cambiar de rama

Para volver a la rama principal (main):

git checkout main


Si quieres ver todas tus ramas:

git branch


La rama con asterisco * es la que tienes activa.

🤝 5. Combinar cambios (merge)

Cuando termines el trabajo en tu rama y quieras integrarlo en main:

1️⃣ Cambia a main:

git checkout main


2️⃣ Trae los últimos cambios de GitHub por si alguien más subió cosas:

git pull origin main


3️⃣ Combina tu rama con main:

git merge nombre-de-tu-rama


Ejemplo:

git merge feature-login


4️⃣ Sube los cambios a GitHub:

git push

💡 Tips útiles

Si quieres borrar la rama local después del merge:

git branch -d nombre-de-tu-rama


Y en remoto:

git push origin --delete nombre-de-tu-rama


Para trabajar en otra rama sin guardar tus cambios actuales:

git stash
git checkout otra-rama
git stash pop   # para recuperar los cambios guardados

🎯 Resumen rápido (la mini-chuleta)
# Crear y cambiar
git checkout -b nueva-rama

# Subir por primera vez
git push -u origin nueva-rama

# Cambiar de rama
git checkout main

# Combinar en main
git merge nueva-rama
git push
