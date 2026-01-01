# Proyecto LaTeX

Este proyecto está basado en LaTeX y tiene como objetivo generar un documento profesional utilizando herramientas y configuraciones modernas. A continuación se explica cómo configurar el entorno de desarrollo y trabajar con el repositorio.

## Instalación

### En Windows (usando MixTeX)

1. **Descargar MiKTeX**
   - Visita el sitio oficial:  
     https://miktex.org/download
   - Descarga el instalador correspondiente a tu versión de Windows.

2. **Instalar MiKTeX**
   - Ejecuta el instalador y sigue las instrucciones.
   - Se recomienda habilitar la opción de instalar paquetes faltantes automáticamente.

3. **Instalar Perl**
   - Algunos flujos de compilación LaTeX y herramientas auxiliares requieren **Perl**.
   - Descarga e instala **Strawberry Perl** desde:  
     https://strawberryperl.com/
   - Durante la instalación, asegúrate de que Perl se agregue al **PATH** del sistema.

4. **Verificar la instalación**
   - Abre la terminal (cmd o PowerShell) y ejecuta:
     ```cmd
     pdflatex --version
     perl --version
     ```
   - Ambos comandos deben responder correctamente.

---

### En Linux (usando TeX Live)

1. **Instalar TeX Live:**
   - En la terminal, ejecuta el siguiente comando:
     ```bash
     sudo apt-get install texlive
     ```

2. **Verificar instalación:**
   - Ejecuta `pdflatex --version` en la terminal para asegurarte de que la instalación fue exitosa.

## Uso de VSCode con LaTeX Workshop

### Instalación de VSCode

1. **Instalar Visual Studio Code:**
   - Ve al [sitio oficial de VSCode](https://code.visualstudio.com/) y descarga la versión adecuada para tu sistema operativo.
   - Sigue las instrucciones para completar la instalación.

2. **Instalar LaTeX Workshop:**
   - Abre VSCode y ve a la vista de extensiones (Ctrl+Shift+X).
   - Busca "LaTeX Workshop" e instálalo.  
*Se recomienda instalar extensiones adicionales relacionadas a latex como 'LaTeX Utilities' y un corrector de ortografia*
## Uso de LaTeX Workshop en VSCode

### 1. Compilación del documento LaTeX

Una vez que hayas abierto tu archivo `main.tex` en VSCode, **LaTeX Workshop** proporcionará varios botones en la barra lateral izquierda para compilar tu documento y ver el resultado.

- **Botón de Compilación (Build)**:
  - En la barra de herramientas superior (en VSCode), verás un botón con el ícono de "Build LaTeX Project .
  - Haz clic en este botón para compilar tu documento LaTeX. La extensión automáticamente detectará el archivo principal (`main.tex` o el archivo principal de tu proyecto).
  - Si estás trabajando en otro archivo `.tex` que no sea el principal, asegúrate de estar en el archivo principal antes de presionar el botón de compilación.

- **Botón de Ver PDF**:
  - Una vez que se haya realizado la compilación correctamente, en la parte superior de la barra de herramientas aparecerá otro botón con el ícono de un PDF.
  - Haz clic en este ícono para abrir el PDF generado. Si la compilación fue exitosa, el documento PDF se abrirá automáticamente en el panel lateral de VSCode.

- **Compilación Automática**:
  - La extensión también soporta compilación automática, pero para compilar manualmente puedes hacer clic en el botón de compilación cada vez que lo necesites (o puedes hacer ctrl + S igual funciona).

### 2. Botón de Limpiar Archivos Auxiliares

Después de compilar tu proyecto, pueden generarse archivos auxiliares (como `.aux`, `.log`, `.out`, etc.). Para eliminarlos:

- **Botón de Limpiar Archivos Auxiliares**:
  - En la barra de herramientas de LaTeX Workshop, hay un botón específico para "Limpiar" estos archivos generados.
  - Este botón generalmente tiene el ícono de una escoba o el texto "Clean" y permite eliminar los archivos auxiliares después de la compilación.

### 3. Asegúrate de estar en el archivo principal (`main.tex`)

- **¿Dónde debes estar para compilar?**
  - Siempre asegúrate de estar en el archivo principal de tu proyecto, como `main.tex`, ya que LaTeX Workshop buscará este archivo para realizar la compilación y generar el PDF.
  - Si estás en otro archivo `.tex` (por ejemplo, en un archivo de capítulos o apéndices), LaTeX Workshop puede no funcionar como esperas.

## Uso de Git para el control de versiones

### 1. Clonar el repositorio

Primero, debes clonar el repositorio en tu máquina local:
```bash
git clone https://github.com/M4gAn4X/Sistemas-Operativos-3.git
```

### 2. Crear tu rama

Una vez que hayas clonado el repositorio, crea una nueva rama para trabajar en tus cambios:
```bash
git checkout -b nombre-de-tu-rama
```

### 3. Añadir tus cambios con `add` y `commit`

Después de realizar los cambios, añade los archivos modificados al área de preparación:
```bash
git add -A
```
Luego, haz un commit con un mensaje descriptivo de lo que has cambiado:
```bash
git commit -m "Descripción de los cambios realizados"
```

### 4. Subir tu rama al repositorio remoto

Para subir los cambios a tu rama en el repositorio remoto, utiliza:
```bash
git push origin nombre-de-tu-rama
```

### 5. Mantener tu rama actualizada

A medida que otros miembros del equipo realicen cambios en el repositorio, es importante mantener tu rama actualizada.

Si estás trabajando en una rama diferente, reemplaza `main` con el nombre de la rama principal

#### Obtener los últimos cambios del repositorio remoto

```bash
git pull origin main
```

#### Resolver conflictos

Si hay conflictos durante el `git pull`, Git te pedirá que los resuelvas. Abre los archivos conflictivos, resuelve los conflictos y luego marca los archivos como resueltos:
```bash
git add archivo-conflictivo
```
Después de resolver los conflictos, haz un nuevo commit:
```bash
git commit -m "Conflictos resueltos"
```
Y finalmente, sube los cambios

### 6. Crear un Pull Request

Una vez que hayas terminado tu trabajo en la rama, puedes crear un pull request (PR) para fusionar tus cambios con la rama principal del repositorio. Esto generalmente se hace desde la interfaz web del repositorio en GitHub o GitLab.

---
