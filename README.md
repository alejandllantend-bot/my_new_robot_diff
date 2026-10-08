# Requisitos

Antes de comenzar con el desarrollo y compilación del proyecto, asegúrate de contar con los siguientes requisitos:

* **Ubuntu 24.04 LTS**
* **ROS 2 Jazzy**
* **Gazebo (GZ)**
* **Visual Studio Code**

## Instalación de ROS 2 Jazzy y Gazebo

Para garantizar que el código compile y funcione correctamente, se recomienda realizar la instalación de **ROS 2 Jazzy** siguiendo la documentación oficial:

* **Documentación oficial de ROS 2 Jazzy:**
  https://docs.ros.org/en/jazzy/Installation.html

También puedes consultar la guía de instalación de **ROS 2 y Gazebo** desarrollada específicamente para este proyecto:

* **Guía de instalación ROS 2 + Gazebo:**
  https://alejandllantend-bot.github.io/diff_robot_docs/Ros2/Conceptos/Instalacion.html

> **Nota:** Se recomienda completar correctamente la instalación y configuración de ROS 2 Jazzy y Gazebo antes de continuar con los siguientes pasos del proyecto.

## Archivo de lanzamiento

### 1. Clonar el repositorio

Clona este repositorio dentro de la carpeta `src` de tu workspace de ROS 2.

Una vez clonado, dirígete a la carpeta principal del workspace y compila el proyecto:

```bash
colcon build
source install/setup.bash
```

### 2. Ejecutar el archivo de lanzamiento

Después de compilar el proyecto, ejecuta el archivo de lanzamiento para visualizar el robot en **RViz** y **Gazebo**:

```bash
ros2 launch my_robot_bringup my_car_gazebo.launch.xml
```

### 3. Controlar el movimiento del robot

Para controlar manualmente el movimiento del robot mediante el teclado, ejecuta:

```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

### ⚠️ Nota

Si al ejecutar el archivo de lanzamiento se presenta un error relacionado con el mundo de Gazebo, realiza una de las siguientes opciones:

* En el archivo del mundo ubicado en la subcarpeta `my_robot_bringup`, desactiva la **línea 17** y activa la **línea 18**.
* También puedes eliminar el archivo `test_my_world_gz.sdf` y crear o utilizar tu propio mundo de Gazebo.

Después de realizar los cambios, vuelve a compilar el workspace antes de ejecutar nuevamente el archivo de lanzamiento.
