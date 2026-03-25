# Sistema de Gestión Mecánica - MiImperio 🛰️

Software desarrollado en *Python* para gestionar el mantenimiento mecánico de la flota espacial del Imperio Galáctico. Este proyecto constituye el **primer entregable** de la asignatura **Programación para Ciencia de Datos** del **Grado en Ciencia e Ingeniería de Datos** en la **Universidad Politécnica de Cartagena (UPCT)**.

## 🛠️ Decisiones Tecnológicas y Metodología

Para el desarrollo y documentación de este proyecto he optado por el siguiente stack tecnológico a diferencia del especificado en el enunciado. Este stack se basa en:

* **Documentación con Quarto (en lugar de MS Word):** Toda la documentación del proyecto no la he redactado directamente Microsoft Word sino que he utilizado **Quarto**, una herramienta de publicación científica que permite escribir el documento en Markdown e integrar comandos de LaTeX específicamente para el formato avanzado de tablas, inserción de imágenes y listas con viñetas. Además, este documento de Quarto va acompañado de archivo de configuración `header_entregable_I.tex` que permite dar formato al documento. He decidido esta opción porque a nivel personal utilizo esta herramienta para la redacción de mis apuntes, prácticas y ejercicios de todas las asignaturas del grado.

* **Diagramas UML con Mermaid (en lugar de UMLet):** Como padezco de problemas de incompatibilidad nativa de la herramienta UMLet con el sistema operativo macOS, he preferido utilizar la herramienta **Mermaid**, la cual ya estoy también familiarizado al utilizarla recientemente para el desarrollo de mis apuntes del `Tema 2 - Programación Orientada a Objetos` y del `Tema 3 - Patrones de Diseño` de esta misma asignatura.

## 📂 Estructura del Repositorio

El proyecto se divide en tres bloques lógicos principales:

```text
pcd_entregable1_alfonso/
├── docs/                # Documentación del proyecto, diagramas UML (Mermaid) y capturas.
├── src/                 # Código fuente de la aplicación.
│   ├── __init__.py      # Inicialización del paquete de código fuente.
│   ├── flota.py         # Núcleo del modelo (POO: Herencia, Abstracción, Encapsulamiento).
│   └── main.py          # Script principal de ejecución y simulación de transacciones.
├── tests/               # Pruebas unitarias para garantizar la robustez del sistema.
│   ├── __init__.py      # Inicialización del paquete de código fuente.
│   └── test_flota.py    # Batería de tests implementada con pytest.
```

## 🪾 Ramas del Repositorio 

El repositorio cuenta con dos ramas principales:

* `main`: Rama principal que contiene el código fuente final del proyecto, la documentación y las pruebas unitarias.
* `development`: Rama de desarrollo donde se han implementado las funcionalidades y se han realizado las pruebas unitarias antes de fusionarlas con la rama `main`.

En el transcurso del desarrollo he utilizado la rama `development` para implementar el código fuente y los test unitarios. Por otro lado, en la rama `main` he ido redactando la documentación a medida que se iba desarrollando el proyecto, por lo que la rama `development` se ha utilizado como una copia de seguridad de la documentación para evitar perderla en caso de algún error o conflicto al fusionar las ramas.

## 🏷️ Etiquetas `tags` Creadas en el Repositorio

A lo largo del ciclo de vida del proyecto, he definido diversas etiquetas para marcar los hitos más importantes y garantizar un control de versiones exhaustivo. He registrado los siguientes *tags*:

* **`v0.1.0-init`**: Marca la configuración inicial del entorno, la creación de la estructura de carpetas y el establecimiento de las plantillas de documentación.
* **`v0.2.0-design`**: Etiqueta la finalización de la fase de diseño del software, incluyendo los diagramas de clases, casos de uso y secuencia modelados en UML.
* **`v0.3.0-implementation`** *(Rama `development`)*: Hito de finalización del código fuente en Python, abarcando la jerarquía de la flota y el sistema de inventarios.
* **`v0.4.0-testing`** *(Rama `development`)*: Certifica la creación y superación exitosa de la batería de pruebas unitarias implementadas con el framework `pytest` y la correcta gestión de excepciones.
* **`v1.0.0-final`**: Versión definitiva y estable del proyecto, creada tras la fusión final en la rama `main`, conteniendo tanto el código evaluable como la documentación completa.

## 🚀 Ejecución del Proyecto

Para ejecutar el proyecto primero debes clonar el repositorio escribiendo en la terminal el siguiente comando:

```bash
git clone https://github.com/alfonsoandressUPCT/pcd_entregable1_alfonso.git
```

Después, debes de asegurarte que tienes instalado Python 3.8 o superior en tu sistema y además, que tengas instalado el gestor de paquetes `pip` para instalar la dependencia de `pytest` para ejecutar las pruebas unitarias. Para instalar `pytest`, puedes ejecutar el siguiente comando en la terminal:

```bash
pip install pytest
```

Finalmente, para ejecutar el script principal de la aplicación desde la raíz del proyecto, puedes utilizar el siguiente comando:

```bash
python src/main.py
```

Y para ejecutar las pruebas unitarias, puedes utilizar el siguiente comando:

```bash
pytest tests/test_flota.py
```

